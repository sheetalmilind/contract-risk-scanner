# Contract Risk Report — TechVendor Ltd.

## Risk Rating
**High** — Section 6 irrevocably assigns all Customer Data to the Vendor, which may be used, commercialized, and disclosed during and after the term without notice or compensation to Customer.

**Critical Summary:** The most dangerous clause is Section 6 (Customer Data), which irrevocably assigns all Customer Data to Vendor for commercialization and disclosure after the term ends, without notice or compensation. The most important customer obligation is the non-renewal notice in Section 4: written notice must be given at least seven (7) days before the end of the current 12-month term, or Customer is liable for the full fees of the renewal term. Before signing, the recommended action is to require deletion of the irrevocable assignment in Section 6, or limit it to a license needed to provide the Services.

## P1 Critical Clauses
| Clause type | Excerpt | Risk explanation |
|---|---|---|
| Auto-renewal without adequate notice (Section 4) | "shall automatically renew for successive twelve (12) month terms unless Customer provides written notice of non-renewal at least seven (7) days prior to the end of the then-current term." | Renewal is automatic and the non-renewal notice window is seven days. Notice received late is ineffective, and Customer is liable for the full fees for the renewal term. |
| Uncapped liability (Section 8) | "Customer's liability to Vendor for any claim arising under or related to this Agreement, including indemnification obligations, breach of confidentiality, and misuse of the Services, shall be unlimited." | Customer's liability has no cap. Vendor's aggregate liability is capped at fees paid in the preceding one month. |
| Possible punitive penalty (Section 2) | "Late payments accrue interest at 1.5% per month." | Late payments carry interest of 1.5% per month. The contract does not describe this as a penalty; it is classed P1 as a possible punitive penalty under the taxonomy. |
| Unilateral data assignment to vendor (Section 6) | "all data, content, and records submitted to or generated through the Services by Customer or its users ("Customer Data") are hereby irrevocably assigned to Vendor." | Customer Data is irrevocably assigned to Vendor. Vendor may use, commercialize and disclose it during and after the term without further notice or compensation to Customer. |

## P2 Major Clauses
| Clause type | Excerpt | Risk explanation |
|---|---|---|
| Broad indemnification (Section 8) | "Customer shall indemnify and hold Vendor harmless from any and all third-party claims, losses, and expenses arising from Customer's use of the Services." | Customer indemnifies Vendor against any and all third-party claims, losses and expenses arising from Customer's use of the Services. No cap applies (see Section 8 liability clause). |
| Exclusivity | — | None found |
| Price escalation trigger (Section 3) | "Vendor may increase the fees charged under this Agreement at any time upon written notice, by up to fifteen percent (15%) per year, without the need for Customer's consent." | Vendor may raise fees up to 15% per year on written notice, without Customer's consent. Continued use is deemed acceptance of the adjusted fees. |
| Customer data ownership ambiguity (Section 6) | "Customer retains ownership of its confidential business information; however," | The clause states Customer retains ownership of its confidential information, then assigns all Customer Data to Vendor. The relationship between these two statements is not clarified. |

## P3 Minor Clauses
| Clause type | Excerpt | Risk explanation |
|---|---|---|
| Termination for convenience timeline (Section 5) | "Either party may terminate this Agreement for convenience by giving the other party thirty (30) days' prior written notice." | Either party may terminate for convenience on 30 days' written notice. Customer receives no refund of prepaid fees on termination. |
| Notice period, breach cure (Section 5) | "fails to cure such breach within thirty (30) days of notice." | Termination for material breach requires a 30-day cure period after notice. |
| Governing law (Section 10) | "This Agreement shall be governed by and construed in accordance with the laws of the State of Delaware, United States of America, without regard to conflict-of-law principles." | Delaware law governs the Agreement. |
| Dispute resolution forum (Section 10) | "The parties submit to the exclusive jurisdiction of the state and federal courts located in Wilmington, Delaware." | Exclusive jurisdiction is in the state and federal courts in Wilmington, Delaware. |

## Key Obligations
### Acme Corp
- Shall pay Vendor the annual subscription fee of USD 120,000, invoiced annually in advance (Section 2).
- Invoices must be paid within thirty (30) days of receipt (Section 2).
- Shall be liable for the full fees for the renewal term if written notice of non-renewal is not received at least seven (7) days prior to the end of the then-current term (Section 4).
- Shall indemnify and hold Vendor harmless from any and all third-party claims, losses, and expenses arising from Customer's use of the Services (Section 8).
- Customer's liability to Vendor, including for indemnification obligations, breach of confidentiality, and misuse of the Services, shall be unlimited (Section 8).
- Shall protect Vendor's non-public information using at least reasonable care and shall not disclose it to third parties except as required to perform this Agreement or as required by law; survives three (3) years after termination (Section 9).
- Neither party may assign this Agreement without the other's written consent (Section 11).

### TechVendor Ltd.
- Shall provide Customer with access to the cloud-based workflow automation platform (the "Services") in accordance with Exhibit A (Section 1).
- Shall use commercially reasonable efforts to make the Services available 99.5% of the time each calendar month, excluding scheduled maintenance (Section 1).
- Warrants that the Services will perform materially in accordance with Exhibit A (Section 7).
- Vendor's aggregate liability to Customer shall not exceed the fees paid by Customer in the preceding one (1) month (Section 8).
- Shall not be liable for indirect, incidental, or consequential damages (Section 8).
- Shall protect Customer's non-public information using at least reasonable care and shall not disclose it to third parties except as required to perform this Agreement or as required by law; survives three (3) years after termination (Section 9).
- Neither party may assign this Agreement without the other's written consent, except that Vendor may assign it to an affiliate or successor (Section 11).

## Run Info
- Input file: input/sample_contract.txt
- Date: 2026-11-04
- Model: Coordinator — sonnet (claude-sonnet-5-5)
- Sub-agents used: clause-agent, obligation-agent, risk-agent (run in parallel as haiku general-purpose agents using each agent's prompt, because the custom agent types were not registered in this session)

---
GATE: FAIL
