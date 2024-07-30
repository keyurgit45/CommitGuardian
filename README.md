# CommitGuardian (Commit Message Checker)

This repository contains a Git hook that ensures commit messages adhere to the [Conventional Commits](https://www.conventionalcommits.org/) specification. This standard helps in creating human and machine-readable commit messages, facilitating better project management and versioning.

## How It Works

CommitGuardian hooks into the Git commit process to validate commit messages against several criteria:

1. **Conventional Commits Structure**:
   - Enforces the structure: `<type>[optional scope]: <description>`.
   - Accepts standard types such as `feat`, `fix`, `chore`, etc.
   - Checks that the type and description are properly formatted.

2. **Title Length**:
   - Ensures the commit title does not exceed 47 characters.

3. **Description Formatting**:
   - Verifies that any description provided is properly formatted with line breaks for readability (suggested max of 50 characters per line).
   - Checks that each line does not exceed 67 characters.

4. **Imperative Mood**:
   - Ensures the commit message uses imperative mood (e.g., "fix" not "fixed").

5. **Scope Validation**:
   - If a scope is provided, it checks against allowed scopes like `parser`, `ui`, `backend`, `api`.

6. **Issue Reference Section**:
   - Supports referencing issues with "Closes" or "Fixes" (case insensitive), ensuring proper format (e.g., `Closes: #123`).
   - Disallows multiple "Closes" or "Fixes" entries to avoid ambiguity.

## Commit Message Structure

A conventional commit message should follow this format:

```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```

### Types Include:
- **feat**: Introduces a new feature.
- **fix**: Patches a bug.
- **BREAKING CHANGE**: Introduces a change that causes the API to break.

For more details on commit types and structure, visit [Conventional Commits](https://www.conventionalcommits.org/).

## Getting Started

1. **Clone this repository**:
   ```bash
   git clone <repository_url>
   ```

2. **Link the commit message script** to your `.git/hooks` directory:
   ```bash
   ln -s /path/to/commit-msg .git/hooks/commit-msg
   ```

3. **Give executable permission** to the hook:
   ```bash
   chmod +x .git/hooks/commit-msg
   ```

4. **Enjoy automated commit message validation!**

## Why Use Conventional Commits?

- **Automated Tools**: Simplifies the creation of automated tools such as changelog generators.
- **Clear Communication**: Helps communicate the intent and scope of changes to teammates and other stakeholders.
- **Semantic Versioning**: Supports semantic versioning by classifying the nature of changes.
