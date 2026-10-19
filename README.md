# Playwright + TypeScript Test Automation Framework

End-to-end UI and API test automation framework built with **Playwright** and **TypeScript**, running in **GitHub Actions** with **Allure** reporting.

> Status: 🚧 Sprint 1 – Foundation in progress

## Applications under test

| Layer | App | URL |
|---|---|---|
| UI | SauceDemo | https://www.saucedemo.com |
| API | Restful-Booker | https://restful-booker.herokuapp.com |

## Tech stack

- Playwright Test (TypeScript) – UI + API in one runner
- Page Object Model + custom fixtures
- Zod/Ajv schema validation, Faker test-data builders
- axe-core accessibility checks, visual regression
- GitHub Actions (PR + nightly, sharded), Allure report on GitHub Pages
- Slack notifications of nightly results
- AI-assisted test generation & triage (Playwright MCP + Claude)

## Planned structure

```
├── tests/
│   ├── ui/          # SauceDemo specs
│   └── api/         # Restful-Booker specs
├── pages/           # Page objects
├── fixtures/        # Custom test fixtures
├── api/             # Typed API client
├── data/            # Test-data builders
├── utils/
├── docs/
└── playwright.config.ts
```

## Quick start (once Sprint 1 lands)

```bash
npm ci
npx playwright install --with-deps
cp .env.example .env
npx playwright test            # all
npx playwright test --grep @smoke
```

## Project plan

See [docs/PLAN.md](docs/PLAN.md). Work is tracked in Jira project **SCRUM**:
https://rabinavidan.atlassian.net/jira/software/projects/SCRUM/boards/1
