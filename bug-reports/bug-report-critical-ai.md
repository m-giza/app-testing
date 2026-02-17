# Bug Report: AI Redaction - False Negative on PESEL Numbers

## Bug ID
`AI-RED-047` | **Priority: Cricital** | **Severity: High**

## Summary
Automated redaction module fails to detect PESEL numbers when embedded in table cells with merged borders

## Steps to Reproduce
1. Upload PDF document containing a table with merged cells
2. Ensure PESEL number is inside a merged cell (ex. "80010112345")
3. Run automated redaction process
4. Download processed document
5. Inspect output for redacted content

## Expected Result
PESEL number should be detected and redacted (black blox overlay + text removal)

## Actual Result
PESEL number remains visible and unredacted in 70% of test cases

## Impact Analysis
| Metric | Value |
|--------|-------|
| Affected documents | ~30% of uploaded files with tables |
| Data Leak Risk | **Critical** |
| Legal Compliance | Violation risk |

## Screenshots
- [Screenshot_1_unredacted_pesel.png]
- [Screenshot_2_expected_redaction.png]
- [Test_Document_Sample.pdf]

## Additional Notes
This is a **regression* - worked correclty in v1.0.3. Issue appeared after v1.1.0 update.

---

**Reported by:** Marsel Giza
**Date:** 2026-02-17
**Status:** Open
