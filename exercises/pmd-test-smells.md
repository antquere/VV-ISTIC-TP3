# Detecting test smells with PMD

In folder [`pmd-documentation`](../pmd-documentation) you will find the documentation of a selection of PMD rules designed to catch test smells.
Identify which of the test smells discussed in classes are implemented by these rules.

Use one of the rules to detect a test smell in one of the following projects:

- [Apache Commons Collections](https://github.com/apache/commons-collections)
- [Apache Commons CLI](https://github.com/apache/commons-cli)
- [Apache Commons Math](https://github.com/apache/commons-math)
- [Apache Commons Lang](https://github.com/apache/commons-lang)

Discuss the test smell you found with the help of PMD and propose here an improvement.
Include the improved test code in this file.

## Answer

Test smells are patterns in the code of a test that might indicate a problem or an area for improvement.

Assertion Roulette:
- Test Smell: The test has multiple assertions, making it hard to understand the exact cause of a failure.
- Improvement: Refactor the test into multiple smaller tests, each focusing on a specific behavior. This makes it easier to identify which part of the test is failing.

Eager Test:
- Test Smell: The test is trying to test too much functionality in a single test case.
- Improvement: Break down the test into smaller, more focused tests. Each test should concentrate on verifying a specific behavior or scenario.

Mystery Guest:
- Test Smell: The test uses external resources (e.g., files, databases) without setting them up or cleaning up properly.
- Improvement: Ensure that the test sets up any necessary resources before running and cleans up afterward. This ensures the test is isolated and doesn't depend on external factors.

Conditional Test Logic:
- Test Smell: The test has conditional logic (if statements) based on certain conditions.
- Improvement: If possible, refactor the test so that each condition is tested in a separate test case. This provides clarity on which conditions are causing test failures.
