# Conventional Commits Types Reference

When analyzing changes, map them to one of the following types strictly:

| Type | Description | Trigger Condition |
|------|-------------|-------------------|
| **feat** | A new feature | Adds new functionality, endpoints, or UI elements. |
| **fix** | A bug fix | Fixes a bug, crash, or incorrect behavior. |
| **docs** | Documentation only changes | Changes to README, comments, or docstrings only. |
| **style** | Styles | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc). |
| **refactor** | Code refactoring | A code change that neither fixes a bug nor adds a feature (e.g., renaming variables, moving files). |
| **perf** | Performance improvement | A code change that improves performance. |
| **test** | Tests | Adding missing tests or correcting existing tests. |
| **build** | Builds | Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm). |
| **ci** | CI configurations | Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs). |
| **chore** | Chores | Other changes that don't modify src or test files. |
| **revert** | Reverts | Reverts a previous commit. |
