# Contract Risk Report — TechVendor Ltd. (input/sample_contract.txt)

## Risk Rating
**High** — Section 6 irrevocably assigns all Customer Data to Vendor for any business purpose, which is a P1 unilateral data assignment, and Section 8 makes Customer's liability unlimited, which is also P1.

### Critical Summary
The most dangerous clause is Section 6, which irrevocably assigns all Customer Data to Vendor for any business purpose during and after the term, without notice or compensation. The most important customer obligation is Section 8, under which Customer's liability to Vendor, including indemnification, is unlimited while Vendor's liability is capped at fees paid in the preceding one month. Before signing, Customer should strike or narrow the Section 6 data assignment.

## P1 Critical Clauses
| Clause type | Excerpt | Risk explanation | Confidence | Confidence reason |
|---|---|---|---|---|
| Auto-renewal without adequate notice | "this Agreement shall automatically renew for successive twelve (12) month terms unless Customer provides written notice of non-renewal at least seven (7) days prior" | Renews automatically for 12 months unless Customer gives non-renewal notice at least 7 days before term end. Late notice is ineffective and Customer owes the full renewal-term fees. | High | Auto-renewal and the 7-day window are stated explicitly. |
| Uncapped liability (Customer) | "Customer's liability to Vendor for any claim arising under or related to this Agreement, including indemnification obligations, breach of confidentiality, and misuse of the Services, shall be unlimited." | Customer's liability is unlimited, while Vendor's liability is capped at one month of fees. | High | The text expressly states the Customer's liability is unlimited. |
| Unilateral data assignment to vendor | "all data, content, and records submitted to or generated through the Services by Customer or its users ("Customer Data") are hereby irrevocably assigned to Vendor." | Customer Data is irrevocably assigned to Vendor, and Vendor may use and commercialise it during and after the term without notice or compensation. | High | Assignment and post-term use rights are explicitly stated. |
| Punitive penalty (late payment interest) | "Late payments accrue interest at 1.5% per month." | Late payments accrue 1.5% monthly interest, which is a financial penalty. The contract does not characterise it as punitive, so this classification is a judgment. | Medium | The rate is stated, but whether it is punitive is an interpretation. |

## P2 Major Clauses
| Clause type | Excerpt | Risk explanation | Confidence | Confidence reason |
|---|---|---|---|---|
| Broad indemnification | "Customer shall indemnify and hold Vendor harmless from any and all third-party claims, losses, and expenses arising from Customer's use of the Services." | Customer indemnifies Vendor against any and all third-party claims, losses and expenses arising from its use of the Services, with no stated cap or fault limitation. | High | The indemnity scope is stated directly. |
| Price escalation trigger | "Vendor may increase the fees charged under this Agreement at any time upon written notice, by up to fifteen percent (15%) per year, without the need for Customer's consent." | Vendor may raise fees up to 15% per year without Customer consent. Continued use is deemed acceptance. | High | The escalation right and consent waiver are explicit. |
| Customer data ownership ambiguity | "Customer retains ownership of its confidential business information; however, all data, content, and records submitted to or generated through the Services by Customer or its users" | The contract says Customer retains ownership of its confidential information, then assigns broadly defined data to Vendor. The scope of "confidential business information" versus "Customer Data" is not defined. | High | The internal tension between the two sentences is visible in the text. |

## P3 Minor Clauses
| Clause type | Excerpt | Risk explanation | Confidence | Confidence reason |
|---|---|---|---|---|
| Termination-for-convenience timeline | "Either party may terminate this Agreement for convenience by giving the other party thirty (30) days' prior written notice." | Either party may terminate for convenience on 30 days' written notice. | High | The notice period is stated explicitly. |
| Notice period (breach cure) | "Either party may terminate immediately upon written notice if the other party materially breaches this Agreement and fails to cure such breach within thirty (30) days of notice." | A 30-day cure period applies before termination for material breach. | High | The cure period is stated explicitly. |
| Termination consequences (refund) | "Upon termination, Customer is not entitled to a refund of any prepaid fees." | Prepaid fees are non-refundable on termination. This relates to termination timing but is not a timeline term, so the classification is a judgment. | Medium | The refund exclusion is explicit, but the taxonomy category is an interpretation. |
| Governing law | "This Agreement shall be governed by and construed in accordance with the laws of the State of Delaware, United States of America, without regard to conflict-of-law principles." | Delaware law governs the Agreement. | High | Governing law is stated explicitly. |
| Dispute resolution forum | "The parties submit to the exclusive jurisdiction of the state and federal courts located in Wilmington, Delaware." | Disputes must be brought exclusively in Wilmington, Delaware courts. | High | The forum is stated explicitly. |

## Key Obligations

### Acme Corp
- Shall pay TechVendor Ltd. the annual subscription fee of USD 120,000, invoiced annually in advance (Section 2).
- Invoices are due within thirty (30) days of receipt (Section 2).
- Shall be liable for the full fees for the renewal term if non-renewal notice is received after the seven (7) day deadline (Section 4).
- Must provide written notice of non-renewal at least seven (7) days prior to the end of the then-current term to prevent automatic renewal (Section 4).
- Liability to TechVendor Ltd. for any claim arising under or related to the Agreement, including indemnification, breach of confidentiality, and misuse of the Services, shall be unlimited (Section 8).
- Shall indemnify and hold TechVendor Ltd. harmless from any and all third-party claims, losses, and expenses arising from Customer's use of the Services (Section 8).
- Shall protect TechVendor Ltd.'s non-public information using at least reasonable care and shall not disclose it to third parties except as required to perform the Agreement or as required by law; this obligation survives for three (3) years after termination (Section 9).

### TechVendor Ltd.
- Shall provide Acme Corp with access to its cloud-based workflow automation platform (the "Services") in accordance with Exhibit A (Section 1).
- Shall use commercially reasonable efforts to make the Services available 99.5% of the time each calendar month, excluding scheduled maintenance (Section 1).
- Warrants that the Services will perform materially in accordance with Exhibit A (Section 7).
- Aggregate liability to Acme Corp shall not exceed the fees paid by Acme Corp in the preceding one (1) month, and shall not be liable for indirect, incidental, or consequential damages (Section 8).
- Must give thirty (30) days' prior written notice to terminate for convenience (Section 5).
- Shall protect Acme Corp's non-public information using at least reasonable care and shall not disclose it to third parties except as required to perform the Agreement or as required by law; this obligation survives for three (3) years after termination (Section 9).
- Shall not assign the Agreement without Acme Corp's written consent, except to an affiliate or successor (Section 11).

## Run Info
- Input file: input/sample_contract.txt
- Date: 2026-11-05
- Model: coordinator Sonnet 5.5; sub-agents on haiku
- Sub-agents used: clause-agent, obligation-agent, risk-agent (the named agent types were not registered in this session, so each ran as a general-purpose haiku agent using its definition's instructions)

---
GATE: FAIL
