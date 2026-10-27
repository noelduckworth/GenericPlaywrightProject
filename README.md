# Generic Playwright Project

A small end-to-end testing starter built with [Playwright](https://playwright.dev/).

## Requirements

- Node.js (LTS recommended)
- npm

## Getting started

Install the dependencies and the browsers used by Playwright:

```bash
npm ci
npx playwright install
```

Run the tests:

```bash
npm test
```

The Playwright configuration currently runs tests from `tests/` in Chromium, Firefox, and WebKit. Install only the browser you need with `npx playwright install chromium`, `npx playwright install firefox`, or `npx playwright install webkit`.

## Useful commands

```bash
npm run test:headed
npm run test:ui
npm run test:debug
npm run report
```

Test results and the HTML report are written to generated folders that are excluded from Git.

## Project layout

- `tests/` contains the tests run by the current configuration.
- `tests-examples/` contains a TodoMVC example.
- `e2e/` contains an additional example spec; the current configuration does not include this folder.
- `playwright.config.ts` configures browsers, test discovery, and reporting.
- `.github/workflows/playwright.yml` runs the tests on pushes and pull requests.

Add or edit tests in `tests/` to cover your own application. Update `baseURL` and the optional `webServer` configuration in `playwright.config.ts` when testing a local app.

## License

ISC