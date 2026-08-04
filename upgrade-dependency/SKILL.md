---
name: upgrade-dependency
description: Upgrade a dependency or framework version and apply the required compatibility changes.
---

# Upgrade Dependency

Upgrade the requested dependency, plugin, framework, build tool, or Java version.

Before making changes:

- Locate where the version is defined.

- Check whether it is managed by Spring Boot, a BOM, a parent POM, dependency management, or a Gradle version catalog.

- Review relevant API changes, release notes, and migration guidance.

- Verify Java, Maven, Gradle, Spring Boot, and framework compatibility.

- Check for required build or configuration changes.

- Review affected source code and tests.

- Check transitive dependency changes and version conflicts.

- Identify removed or deprecated APIs.

- Determine whether code, configuration, or data migration is required.


Make only the changes required for the upgrade. Do not upgrade unrelated dependencies or perform unrelated refactoring.


Use the project's existing Maven or Gradle wrapper and dependency management conventions.



After the upgrade:


- Run the relevant tests.

- Run the full build or verification task.

- Confirm that the expected version is resolved.

- Check for new warnings, deprecations, or dependency conflicts.

- Review the final diff for unrelated changes.


Report:


- the previous and new version,

- the files and compatibility changes made,

- the validation commands and their results,

- any remaining risks, warnings, or manual migration steps.



Do not claim success if the build or tests still fail.

