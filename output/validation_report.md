# Validation Report — Contract Risk Scanner

## 1. Correctness — rating and any unsupported findings
Reviewed `output/risk_report.md` against `input/sample_contract.txt`.

**Rating: Medium.** Quotes, figures and the High / GATE: FAIL outcome are correct, but one obligation is wrong and one classification is unsupported.

- **Wrong:** Section 11 is mis-stated. The report says TechVendor may not assign without Acme's consent, except to an affiliate or successor. The contract says neither party may assign without the other's consent, and only Vendor may assign to an affiliate or successor. The restriction belongs to Acme.
- **Unsupported:** "Late payments accrue interest at 1.5% per month" is classed as a P1 "punitive penalty". The contract never calls it punitive, and the report itself admits this is a judgment. CLAUDE.md forbids adding interpretations not in the contract. The overall result is unaffected because other P1 findings exist.
- **Judgment call:** the no-refund clause (Section 5) is placed in P3, but it is not in the CLAUDE.md taxonomy.
- **Weak excerpt:** the "Customer data ownership ambiguity" excerpt is cut off mid-sentence.

## 2. Completeness — gaps against the spec
Checked against CLAUDE.md and `coordinator.md`.

- Present: section order, Confidence and Confidence reason columns, title, Run Info fields, trailing `GATE: FAIL`, High rating.
- **Sub-agents:** the named agents (`clause-agent`, `obligation-agent`, `risk-agent`) were not registered and ran as general-purpose haiku agents.
- **Key Obligations incomplete:** Acme's late-payment interest (S2), acceptance of fee increases by continued use (S3), non-refundable prepaid fees (S5) and the assignment restriction (S11) are missing.
- **Heading depth:** "Critical Summary" is an H3 under Risk Rating, not covered by `coordinator.md`.
- **Run date:** 2026-11-05, while the checks were run on 2026-11-06.

## 3. Robustness — broken-input result before the fix
Input `input/broken_input.txt` is one line: `zx9 ;;; ### ??? lorem 0000 <<>>`.

- No crash. All three sub-agents ran and returned valid markdown.
- The merged report said **Risk Rating: Low**, "None found" in P1, P2 and P3, no obligations, and **GATE: PASS**.
- The risk-agent noted in prose that the input is not a contract and that the Low rating should not be relied on, but the rating and gate did not reflect that.
- Consequence: an unreadable file received a passing gate. The three agent calls were also wasted.

## Issue Fixed — problem, change made, evidence from the re-run
**Problem:** the coordinator had no input validation, so non-contract input produced a Low rating and `GATE: PASS`.

**Change made** (`coordinator.md`, new step 1b, before sub-agents launch):
- The file is treated as unreadable if it is empty, has fewer than 20 words, or has no contract language (party names, "Agreement"/"Contract" wording, headed clauses, shall/must/agrees).
- If unreadable, no sub-agents run. The report states **Not assessable**, explicitly forbids a Low rating, and ends with `GATE: FAIL (input not assessable — fail-safe)`.
- `GATE: PASS` is never emitted for unassessable input.

**Evidence from the re-run** (`output/risk_report_broken_input.md`):
- Risk Rating: **Not assessable** (was Low).
- Sub-agents used: none (was three).
- Gate: **GATE: FAIL** with the not-assessable note (was PASS).
- Caveat: the re-run applied the new step manually as the coordinator. The validation is a prompt instruction, not code, so it relies on the coordinator following it. The re-run was written to a separate file so the real `output/risk_report.md` was not overwritten.
- Design note: `GATE: FAIL` was chosen so the output stays within CLAUDE.md's binary gate. It means "failed safe", not "a P1 was found". A distinct `GATE: ERROR` value would be clearer but would require changing CLAUDE.md.
