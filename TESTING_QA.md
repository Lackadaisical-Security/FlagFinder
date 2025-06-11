# FlagFinder Testing & QA

## Unit Tests
- Each plugin (Text, Audio, Image, API) has unit tests in `/test/`
- Example: `TextPlugin.test.ts` covers basic flagging

## End-to-End Tests
- Simulate full pipeline: input → plugin → ML → output
- Use Playwright for UI E2E tests

## Sample Data
- Synthetic chat logs, audio snippets, screenshots in `/test/data/`
- Labeled examples for ML in `/ml/data/`

## CI Pipeline
- GitHub Actions: run tests on push/PR
- Lint, build, and test all modules

## Coverage
- Jest for code coverage

---

See README for test commands and contributing guidelines.
