---
name: git-commit-generator
description: Generate clear, standardized git commit messages based on code changes (diffs), following Conventional Commits specification.
---

# Git Commit Generator

## Description
This skill analyzes code changes (git diffs) and generates semantic, structured commit messages. It ensures that commit messages are concise, descriptive, and follow the Conventional Commits standard (e.g., `feat:`, `fix:`, `docs:`).

## Usage Scenario
Trigger this skill when:
- The user asks to "write a commit message" or "generate a commit".
- The user asks "what did I change?" and expects a summary suitable for a commit.
- You need to propose a commit message for a set of changes you just made.

## Instructions

1.  **Analyze the Changes**:
    *   Read the provided `git diff` or the changes in the current context.
    *   Identify the scope of changes (e.g., specific component, file, or module).
    *   **Determine the type of change**: Refer to `resources/conventional-commits-types.md` for the strict definition of types (feat, fix, docs, etc.).

2.  **Formulate the Commit Message**:
    *   Follow the structure defined in `templates/commit-message.txt`.
    *   **Subject Line**:
        *   Format: `<type>(<scope>): <subject>`
        *   Use imperative mood ("add" not "added", "change" not "changes").
        *   No period at the end.
        *   Keep it under 50 characters if possible.
    *   **Body** (Optional but recommended for non-trivial changes):
        *   Separate from subject with a blank line.
        *   Explain *what* and *why* vs. *how*.
        *   Use bullet points for multiple changes.

3.  **Output Format**:
    *   Provide the commit message in a code block.
    *   If there are multiple logical changes, suggest splitting them into multiple commits or provide alternative messages.

## Examples

### Example 1: Simple Documentation Update
**Input:**
User: "Write a commit message for these changes."
Diff:
```diff
diff --git a/README.md b/README.md
index 431f2eb..e727fe1 100644
--- a/README.md
+++ b/README.md
@@ -10,6 +10,6 @@
 ## Quickstart
 
-1. Clone the repo.
+1. Clone this repository.
```

**Output:**
```text
docs: update quickstart instructions in README

Refine the cloning step for better clarity.
```

### Example 2: Feature with multiple files
**Input:**
User: "Commit these changes for the login button."
Diff shows changes in `src/components/Button.tsx` (added `isLoading` prop) and `src/views/Login.tsx` (passed `loading` state).

**Output:**
```text
feat(auth): add loading state to login button

- Add `isLoading` prop to Button component to support visual feedback
- Connect login form submission state to Button in Login view
- Prevent double submission while request is in progress
```
