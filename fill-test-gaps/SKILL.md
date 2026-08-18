---
name: fill-test-gaps
description: Find meaningful test gaps in current changes or a specified target and add only valuable, non-duplicative tests.
---

Analyze the current changes or the user-specified class, component, or area and add tests only for meaningful coverage gaps.

## Workflow

1. Determine the scope:
   - if no target is specified, inspect `git status` and `git diff` and focus on changed behavior and regression risks,
   - otherwise analyze only the specified target.

2. Review the existing tests and understand what behavior they already check.

3. Identify meaningful gaps such as:
   - untested branches or edge cases,
   - boundary conditions,
   - error and validation paths,
   - important state transitions,
   - externally visible contracts,
   - regression risks introduced by the change.

4. Select the smallest useful set of new tests.

   Each new test must protect a distinct behavior, failure mode, boundary condition, contract, or regression risk.

5. Do not add tests that:
   - differ only by insignificant input values,
   - test trivial getters, setters, constructors, or delegation,
   - verify implementation details without protecting behavior

6. Use parameterized tests when several inputs verify the same rule and it improves clarity.

7. Follow the project's existing test framework, naming, assertions, mocking style, fixtures, and structure.

8. Add only the selected tests.

9. Run the relevant tests and review every newly added test. Remove or consolidate any test that does not provide distinct value.

If no meaningful gaps exist, do not add tests.