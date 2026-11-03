# Contract Risk Report: sample_contract.txt

## Overall Risk Rating
**High** — three P1 (Critical) findings were identified.

Agreement: Software-as-a-Service Agreement, effective January 1, 2025, between Acme Corp ("Customer") and TechVendor Ltd. ("Vendor").

| Severity | Count |
|----------|-------|
| P1 Critical | 3 |
| P2 Major | 3 |
| P3 Minor | 3 |

## P1 Critical Findings

| Clause type | Excerpt | Risk explanation |
|-------------|---------|------------------|
| Auto-renewal without adequate notice (§4) | "automatically renew for successive twelve (12) month terms unless Customer provides written notice of non-renewal at least seven (7) days prior to the end of the then-current term. Notice received after such period shall be ineffective, and Customer shall be liable for the full fees for the renewal term." | The agreement renews automatically. The non-renewal window is only 7 days, and late notice is ineffective and makes Customer liable for the full renewal-term fees. |
| Uncapped liability (§8) | "Customer's liability to Vendor for any claim arising under or related to this Agreement, including indemnification obligations, breach of confidentiality, and misuse of the Services, shall be unlimited." | Customer's liability is unlimited. Vendor's liability is capped at "the fees paid by Customer in the preceding one (1) month", so the exposure is one-sided. |
| Unilateral data assignment to Vendor (§6) | "all data, content, and records submitted to or generated through the Services by Customer or its users ("Customer Data") are hereby irrevocably assigned to Vendor. Vendor may use, analyze, aggregate, commercialize, and disclose Customer Data ... during and after the term of this Agreement, without further notice or compensation to Customer." | Customer Data is irrevocably assigned to Vendor. Vendor may commercialize and disclose it during and after the term, with no notice or compensation. |

## P2 Major Findings

| Clause type | Excerpt | Risk explanation |
|-------------|---------|------------------|
| Price escalation trigger (§3) | "Vendor may increase the fees charged under this Agreement at any time upon written notice, by up to fifteen percent (15%) per year, without the need for Customer's consent." | Vendor can raise fees at any time without consent, by up to 15% per year. "Continued use of the Services constitutes acceptance of the adjusted fees." |
| Broad indemnification (§8) | "Customer shall indemnify and hold Vendor harmless from any and all third-party claims, losses, and expenses arising from Customer's use of the Services." | The indemnity covers any and all third-party claims arising from Customer's use of the Services. It is one-directional, and no Vendor indemnity appears in the contract. |
| Customer data ownership ambiguity (§6) | "Customer retains ownership of its confidential business information; however, all data, content, and records ... are hereby irrevocably assigned to Vendor." | The clause says Customer "retains ownership" of confidential business information, but assigns all Customer Data to Vendor. The contract does not say how the two statements relate. |

## P3 Minor Findings

| Clause type | Excerpt | Risk explanation |
|-------------|---------|------------------|
| Termination-for-convenience timeline (§5) | "Either party may terminate this Agreement for convenience by giving the other party thirty (30) days' prior written notice." | Either party may terminate on 30 days' notice. "Upon termination, Customer is not entitled to a refund of any prepaid fees." |
| Governing law (§10) | "governed by and construed in accordance with the laws of the State of Delaware, United States of America" | Delaware law governs. The contract states Vendor's place of business is in London, United Kingdom. |
| Dispute resolution forum (§10) | "The parties submit to the exclusive jurisdiction of the state and federal courts located in Wilmington, Delaware." | Disputes go exclusively to the courts in Wilmington, Delaware. |

## Other Observations (not classified under the severity taxonomy)
- §2: "Late payments accrue interest at 1.5% per month."
- §8: Vendor "shall not be liable for indirect, incidental, or consequential damages."
- §7: Services are provided "AS IS" apart from the warranty that they will perform materially in accordance with Exhibit A.
- §11: "Vendor may assign it to an affiliate or successor"; Customer needs Vendor's written consent to assign.
- §5: Customer is not entitled to a refund of prepaid fees on termination.
- Signature blocks (names, titles, dates) are blank in the text provided.

## Key Obligations

### Customer (Acme Corp)
- Pay the annual subscription fee of USD 120,000, invoiced annually in advance, due within 30 days of receipt (§2).
- Pay any fee increases (up to 15% per year) from the next invoice after notice (§3).
- Give written non-renewal notice at least 7 days before the end of the term to avoid renewal (§4).
- Indemnify Vendor against third-party claims arising from Customer's use of the Services (§8).
- Accept unlimited liability for claims arising under or related to the Agreement (§8).
- Protect Vendor's non-public information with at least reasonable care; this survives 3 years after termination (§9).
- Obtain Vendor's written consent before assigning the Agreement (§11).

### Vendor (TechVendor Ltd.)
- Provide access to the cloud-based workflow automation platform per Exhibit A (§1).
- Use commercially reasonable efforts to achieve 99.5% monthly availability, excluding scheduled maintenance (§1).
- Warrant that the Services will perform materially in accordance with Exhibit A (§7).
- Protect Customer's non-public information with at least reasonable care; this survives 3 years after termination (§9).
- Give written notice of fee increases (§3) and 30 days' notice for termination for convenience (§5).

## Summary of Results
| Area | Result |
|------|--------|
| P1 findings | 3 (auto-renewal, uncapped Customer liability, data assignment) |
| P2 findings | 3 (fee escalation, broad indemnity, data ownership ambiguity) |
| P3 findings | 3 (termination timeline, governing law, forum) |
| Overall risk | High |

GATE: FAIL
