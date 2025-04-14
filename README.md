# Github Action. Continuous Integration

This repository uses a GitHub Actions workflow (.github/workflows/ci-pipeline.yml) for Continuous Integration:

Triggers: Runs automatically on every push to the main branch and can be triggered manually.
Runner: Uses ubuntu-latest.
Steps:
Checks out the repository code.
Sets up Java 11 (Temurin distribution) and enables Maven dependency caching.
Downloads dependencies using mvn dependency:go-offline.
Compiles and runs unit tests using mvn test.
Packages the application into a WAR file using mvn package -DskipTests.
