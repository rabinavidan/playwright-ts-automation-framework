# Project Plan – Playwright TS Automation Framework

## Goal
Build a production-style, portfolio-ready test automation framework covering UI and API layers, with CI/CD, reporting and AI-assisted testing.

## Scope
- **UI:** SauceDemo – login, inventory/sorting, cart & checkout, visual + a11y
- **API:** Restful-Booker – auth, booking CRUD, schema & negative tests
- **Out of scope:** mobile, performance/load testing

## Epics & stories (Jira)

### SCRUM-5 Framework foundation & project setup
- SCRUM-10 Initialize Playwright + TypeScript project
- SCRUM-11 Environment & config management
- SCRUM-12 Page Object Model base & custom fixtures

### SCRUM-6 UI test suite – SauceDemo
- SCRUM-13 Login tests (standard, locked-out, invalid users)
- SCRUM-14 Inventory & sorting tests
- SCRUM-15 Cart & checkout end-to-end flow
- SCRUM-16 Visual regression & accessibility checks

### SCRUM-7 API test suite – Restful-Booker
- SCRUM-17 API client & auth token handling
- SCRUM-18 Booking CRUD tests
- SCRUM-19 Schema validation & negative API tests
- SCRUM-20 Test data builders (faker)

### SCRUM-8 CI/CD & reporting
- SCRUM-21 GitHub Actions pipeline (PR + nightly)
- SCRUM-22 Allure + HTML reports published to GitHub Pages
- SCRUM-23 Slack notification of test results

### SCRUM-9 Quality, documentation & AI-assisted testing
- SCRUM-24 Flaky-test strategy & tagging
- SCRUM-25 README, architecture docs & contribution guide
- SCRUM-26 AI-assisted test generation & failure triage

## Milestones

| Sprint | Dates | Focus | Stories |
|---|---|---|---|
| 1 – Foundation | Oct 19 – Nov 2, 2026 | Skeleton, config, POM, API client, first tests, CI | SCRUM-10, 11, 12, 13, 17, 21 |
| 2 – Core suites | Nov 2 – Nov 16 | UI + API coverage | SCRUM-14, 15, 18, 19, 20 |
| 3 – Polish | Nov 16 – Nov 30 | Reporting, visual/a11y, flaky strategy, AI, docs | SCRUM-16, 22, 23, 24, 25, 26 |

## Definition of Done
- Test passes on Chromium, Firefox, WebKit (UI) and in CI
- No hard waits; locators use role/test-id
- Code reviewed via PR, lint passes
- Jira story updated with PR link

## Risks
- Public demo apps may be slow/unavailable → retries in CI, health-check before run
- Restful-Booker data resets → every test creates its own data
