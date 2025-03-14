# Cypress Syllabus

**Week 1: Introduction to Cypress & Setup**

*   What is Cypress? Key Features and Advantages.
*   Installation and Configuration.
*   Directory Structure Overview.
*   Writing Your First Test: `describe`, `it`, `cy.visit`.

**Week 2: Cypress Selectors & Actions**

*   Understanding Selectors: CSS Selectors, Cypress Best Practices.
*   Working with Different Element Types: Inputs, Buttons, Links.
*   Common Actions: `cy.get`, `cy.click`, `cy.type`, `cy.clear`.
*   Assertions: Basic Assertions with `should`.

**Week 3: Advanced Assertions & Debugging**

*   Advanced Assertions: `have.text`, `have.value`, `be.visible`, `be.checked`.
*   Debugging Cypress Tests: Cypress Runner, Developer Tools.
*   Using `cy.pause()` and `cy.debug()`.
*   Time Travel Feature.

**Week 4: Working with External Data & Fixtures**

*   Using Fixtures for Test Data.
*   Loading and Using JSON Fixtures.
*   Dynamic Data and Variables.
*   `Cypress.env()` and Configuration Files.

**Week 5: Network Requests & Stubbing**

*   Intercepting Network Requests with `cy.intercept`.
*   Stubbing Responses for Testing Scenarios.
*   Verifying Request Payloads and Headers.
*   Testing Error Handling.

**Week 6: Custom Commands & Plugins**

*   Creating Custom Commands for Reusable Actions.
*   Extending Cypress Functionality with Plugins.
*   Installing and Configuring Plugins (e.g., `cypress-xpath`).

**Week 7: Working with Iframes & Shadow DOM**

*   Accessing Elements within Iframes.
*   Understanding and Interacting with Shadow DOM.
*   Using `shadow()` command.

**Week 8: Cross-Origin Testing & Cookies/Local Storage**

*   Enabling Cross-Origin Testing with `experimentalSessionSupport`.
*   Working with Cookies: `cy.getCookie`, `cy.setCookie`, `cy.clearCookie`.
*   Managing Local Storage: `cy.clearLocalStorage`.

**Week 9: Test Organization & Reporting**

*   Structuring Test Suites for Maintainability.
*   Using Tags for Test Filtering.
*   Generating Test Reports (e.g., Mochawesome, Cypress Dashboard).

**Week 10: CI/CD Integration & Parallelization**

*   Integrating Cypress with Continuous Integration (CI) Systems (e.g., GitHub Actions, CircleCI).
*   Running Tests in Parallel for Faster Execution.
*   Cypress Cloud for Test Recording and Management.
