# Playwright: From Zero to Hero

**Week 1: Foundations & Installation**

*   Introduction to Playwright: Cross-browser automation.
*   Playwright vs. Selenium, Cypress.
*   Node.js and NPM setup (Prerequisites).
*   Installing Playwright: `npm install -D @playwright/test`.
*   Project setup: `npx playwright install`.
*   Basic Playwright script structure: `test()`, `expect()`.

**Week 2: Locators & Actions**

*   Understanding Locators: CSS, XPath, Text, and ID locators.
*   Locator priority and best practices.
*   Working with Actions: `click()`, `fill()`, `type()`, `hover()`, `press()`.
*   Handling Alerts and Dialogs.
*   Frames and iframes.

**Week 3: Assertions & Expectations**

*   Introduction to Assertions: Validating element states and values.
*   `expect()` API in detail: `toBeVisible()`, `toBeChecked()`, `toHaveText()`, `toHaveAttribute()`.
*   Soft Assertions vs. Hard Assertions.
*   Custom Assertions (basic).

**Week 4: Page Object Model (POM)**

*   Introduction to the Page Object Model design pattern.
*   Benefits of using POM: Maintainability, Reusability.
*   Implementing POM: Creating Page classes and methods.
*   Using POM in test scripts.

**Week 5: Advanced Locators & Selectors**

*   Using `getByRole()`, `getByLabel()`, `getByPlaceholder()`, `getByAltText()`, `getByTitle()`
*   Text matching: exact matches, partial matches, regular expressions.
*   Locator chaining and filtering.
*   Debugging locator issues.

**Week 6: Configuration & Parallel Execution**

*   Playwright Configuration File: `playwright.config.ts/js`.
*   Configuring Browsers, Devices, and Viewports.
*   Setting up environments: baseURL, timeouts.
*   Parallel execution: running tests concurrently.
*   Sharding tests across multiple machines.

**Week 7: Test Hooks & Reporters**

*   Test Hooks: `beforeAll()`, `beforeEach()`, `afterEach()`, `afterAll()`.
*   Using Hooks for setup and teardown.
*   Built-in Reporters: List, HTML, JUnit.
*   Custom Reporters (basic).

**Week 8: API Testing with Playwright**

*   Introduction to API Testing using Playwright.
*   Making API requests: `request.get()`, `request.post()`, `request.put()`, `request.delete()`.
*   Asserting API responses: Status codes, Headers, JSON body.
*   API Authentication.

**Week 9: Visual Regression Testing**

*   Introduction to Visual Regression Testing.
*   Taking screenshots with Playwright.
*   Comparing screenshots for visual differences.
*   Setting up baseline screenshots.
*   Tools and best practices for Visual Regression Testing.

**Week 10: Continuous Integration (CI/CD)**

*   Integrating Playwright with CI/CD pipelines.
*   Examples using GitHub Actions, GitLab CI, or Jenkins.
*   Running Playwright tests in headless mode.
*   Generating reports in CI/CD.

**Week 11: Advanced Topics (Optional)**

*   Shadow DOM.
*   WebSockets and Network Interception.
*   Performance Testing with Playwright (basic).
*   Code Coverage.

**Week 12: Project & Review**

*   Working on a larger project using Playwright.
*   Applying learned concepts.
*   Code review and best practices.
*   Q&A and final thoughts.
