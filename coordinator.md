# Coordinator — Financial Contract Risk Report
## Task
Produce a contract risk report for the file named in the request
(default: input/sample_contract.txt). Follow CLAUDE.md.
## Steps
1. Read the contract file once using the Read tool.
2. In a single step, launch these three sub-agents IN PARALLEL.
Pass each one the full contract text — they do not share your context:
- clause-agent → P1/P2/P3 clause findings table
- obligation-agent → Key obligations for each party
- risk-agent → Overall risk rating + critical summary
3. Wait for all three to finish. Merge their sections in this order;
do not rewrite or paraphrase any finding, and keep the Confidence and
Confidence reason columns on every clause row:
Risk Rating → P1 Critical Clauses → P2 Major Clauses →
P3 Minor Clauses → Key Obligations → Run Info
   Severity filter: if the request contains `--severity P1`, launch ONLY
   clause-agent and risk-agent (skip obligation-agent), omit the P2 Major
   Clauses, P3 Minor Clauses and Key Obligations sections from the report,
   and add this line directly under the Risk Rating section:
   "Filter applied: --severity P1 (P2/P3 findings and key obligations omitted)."
4. Append GATE: FAIL if any P1 finding exists, otherwise GATE: PASS.
5. Write the result to output/risk_report.md.
## Output format (output/risk_report.md)
# Contract Risk Report — <vendor name or file name>
## Risk Rating
## P1 Critical Clauses | Clause type | Excerpt | Risk explanation | Confidence | Confidence reason |
## P2 Major Clauses | Clause type | Excerpt | Risk explanation | Confidence | Confidence reason |
## P3 Minor Clauses | Clause type | Excerpt | Risk explanation | Confidence | Confidence reason |
## Key Obligations
## Run Info (input file · date · model · sub-agents used)
---
GATE: FAIL ← if any P1 clause found
GATE: PASS ← if no P1 clauses found