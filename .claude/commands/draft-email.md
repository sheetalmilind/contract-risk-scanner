---
description: Draft a 5-line executive summary email from a risk report
argument-hint: <risk-report-path>
---
Read the risk report at $ARGUMENTS.
Write a 5-line executive summary email to output/summary_email.md, one line each:
- Line 1: Subject line
- Line 2: One-sentence risk rating
- Lines 3-4: Two critical findings (P1 if any, else P2), one per line
- Line 5: Recommended action before signing
Rules:
- Use only facts stated in the report. Do not add facts, vendor names, dates or values not in it.
- Write only to output/. Never write to input/.
- Print the email after saving.
