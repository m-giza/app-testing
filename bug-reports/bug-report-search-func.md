# Bug Report: Search - Invalid Custodian Metadata in Undocked Document View

> **Portfolio Notice**: Anonymized example. No client data or screenshots included
> Technical details reflect methodology, not production specifics.

## Bug ID
`FUNC-SEARCH-033` | **Priority: High** | **Severity: High**

## Summary

Custodian metadata displayed in the **Undocked Document Viewer** contains inconsistent fields compared to the **Docked (Embedded) Viewer**

## Steps to reproduce
1. Locate main navbar -> click search with a loop next to it
2. Search for any custodian from this year (ex. T&F_12_01_2026_CT)
3. Open any document from results list
4. Observe metadata panel (count and field names)
5. Undock the document via "Undock Embedded Viewer" button
6. Observe metadata panel in undocked view

## Expected vs Actual
| Aspect | Expected | Actual |
| ------ | -------- | ------ |
| **Fields Count** | 40 standard metadata fields | 43 fields (3 extra) |
| **Field Content** | Consistent client-facing data | Includes internal/debug fields |
| **Data Integrity** | Matches database record | Discrepancy in specific fields |

## Analysis (API & DevTools)
Investigated using **Chrome DevTools Network Tab** to compare API responses for both view modes.

### 1. Endpoint Comparison
Observation: Endpoint is identical, suggesting issue lies in the backend.

### 2. Response Payload Difference (anonymized)
// Docked View - Correct structure
{
 "docInfo": [
        {
            "name": "Application",
            "value": "Microsoft Outlook Email Message"
        },
        {
            "name": "Custodian",
            "value": "anonymized_user"
        }
            // ... 38 more standard fields
        
}
// Undocked View - Extra Fields
 {
 "docInfo": [
          {
            "name": "Application",
            "value": "Microsoft Outlook Email Message"
          },
          {
            "name": "Custodian", 
            "value": "anonymized_user"
            // ... 38 more standard fields
          {
            "name": "internal_debug_flag":
            "value": "true"
          },
          {
            "name": "legacy_system_id",
            "value": "xxx_xxx"
          },
          {
            "name": "cache version",
            "value": "v1.2.3"
          }

## Impact Analysis
| Area | Impact Level | Description |
|------|--------------| ----------- |
| Data Integrity | **High** | Inconsistent data representation |
| Security | **Medium** | Internal/debug fields exposed to end users |
| User Experience | **Medium** | Confusion for reviewers comparing data |

## Environment
Browser: Chrome(Latest
Environment: Production
Tools: Chrome DevTools (Network Tab)

---

**Reported by:** Marsel Giza
**Date:** 2026-02-17
**Status:** Open
