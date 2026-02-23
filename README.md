#  My Testing Portfolio

This is where I document my learning process and workflow as a software tester. All test cases were manually executed on the [Buggy Cars Rating](https://buggy.justtestit.org/) demo application.

---

## What will you find here?

###  Manual Test Cases

| ID | Name | Type | Status |
|----|------|------|--------|
| [TC-Reg-001](https://github.com/m-giza/app-testing/blob/main/test-cases/TC-Reg-001_atomic.md) | Weak password validation | Functional (Negative) | ✅ Ready |
| [TC-Reg-002](https://github.com/m-giza/app-testing/blob/main/test-cases/TC-Reg-002_atomic.md) | Password mismatch validation | Functional (Negative) | ✅ Ready |
| [TC-Reg-003](https://github.com/m-giza/app-testing/blob/main/test-cases/TC-Reg-003_atomic.md) | Successful registration | Functional (Positive) | ✅ Ready |
| [TC-Login-001](https://github.com/m-giza/app-testing/blob/main/test-cases/TC-Login-001_atomic.md) | Login after registration | Functional (Positive) | ✅ Ready |
| [TC-Logout-001](https://github.com/m-giza/app-testing/blob/main/test-cases/TC-Logout-001_atomic.md) | Logout | Functional (Positive) | ✅ Ready |
| [TC-Vote-001](https://github.com/m-giza/app-testing/blob/main/test-cases/TC-Vote-001_smoke.md) | Voting for a car model | Smoke | ✅ Ready |

###  Checklists

| ID | Scope | Status |
|----|--------|--------|
| [CL-Reg-001](https://github.com/m-giza/app-testing/blob/main/checklists/CL-Reg.md) | User registration | ✅ Ready |
| [CL-Vote-001](https://github.com/m-giza/app-testing/blob/main/checklists/CL-Vote.md) | Car voting | ✅ Ready |

### API Testing

| Artefact | Description | Status |
|----------|-------------|--------|
| [`API-CRUD-Orders.postman_collection.json`](assets/API-CRUD-Orders.postman_collection.json) | CRUD flow on ReqRes API:<br>• POST → extract ID → GET → DELETE<br>• Assertions in tests<br>• Dynamic environment variables | ✅ Ready |

### Bug Reports

Sanitized examples demonstrating my approach to defect reporting.

| ID | Component | Issue Summary | Severity | Status |
|----|-----------|---------------|----------|--------|
| [AI-RED-047](https://github.com/m-giza/app-testing/blob/main/bug-reports/bug-report-critical-ai.md) | AI Redaction Module | False negative on PESEL detection in merged table cells | High | Open |
| [FUNC-SEARCH-033](https://github.com/m-giza/app-testing/blob/main/bug-reports/bug-report-search-func.md) | Search / Document Viewer | Metadata inconsistency between docked and undocked views | High | Open |

### Tools & Environment (used in this repository)

- Chrome DevTools (network inspection, console validation)
- Postman (REST API testing, collection variables)
- JavaScript assertions (response validation in Postman)
- Git (version control)
- GitHub (documentation & repository management)

---

## My Workflow

### Manual Testing Approach

In my daily work, I prioritize **clarity and precision in documentation**. In this portfolio:
- Each test has **a single objective** - I do not combine registration, login, and voting into one scenario.
- **I do not rely solely on UI messages** - I always validate the system state (e.g., refreshing after registration to confirm the account was actually created).
- I pay attention to **UX issues**, even if they are not functional bugs (e.g., missing redirect after registration).

### API Testing Approach

The Postman collection (`API-CRUD-Orders`) is my first publicly shared work in this area. It demonstrates:
- C-R-D flow (Create, Read, Delete) on ReqRes API,
- Dynamic variable chaining (`recordId`),
- Basic assertions in the "Tests" section.

This collection demonstrates foundational REST API testing practices and structured request chaining.

### Why are these artifacts simple?

I am not including complex cases from my professional work (e.g., eDiscovery, AI modules) because:
- I wanted to create a **clear entry point** for recruiters,
- This portfolio focuses on **manual testing fundamentals**, which are universal,
- Complex cases often contain confidential data - these are **100% public and safe**.

---

## Important Notes

- All credentials (`JHwell@32`, `Jnth@n!23`) are fictional test accounts
- Checklists only include what I have actually tested
- Buggy Cars is an official training platform

---

## Use of Artificial Intelligence

AI was used exclusively for:
- Improving formatting of `.md` files (GitHub syntax, tables, headers)
- Refining language in descriptions (without altering technical content)

**All tests, data, logic, and validations were executed 100% by me.**

---
## Contact

- **GitHub:** [@m-giza](https://github.com/m-giza)

> This portfolio is actively maintained. Planned additions: extended Postman collections and Playwright scripts. Last updated: February 23, 2026
