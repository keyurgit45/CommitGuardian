# CommitGuardian (Commit Message Checker)

This repository contains a hook that ensures commit messages follow the Conventional Commits specification, which is a standard for adding human and machine-readable meaning to commit messages.

## How It Works

The tool hooks into the commit process, evaluating commit messages based on the Conventional Commits specification. If a commit message does not comply with the structure, the commit is rejected.

### Commit Message Structure

A conventional commit message should look like this:

```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```

Types include:
- `feat`: Introduces a new feature.
- `fix`: Patches a bug.
- `BREAKING CHANGE`: Introduces a change that causes the API to break.

For more details on commit types and structure, visit [Conventional Commits](https://www.conventionalcommits.org).

## Getting Started

1. Clone this repository.
2. Link the commit message script to your `.git/hooks` directory.
3. give executable permission to the hook using chmod.
4. Enjoy automated commit message validation!

## Why Use Conventional Commits?

- Simplifies the creation of automated tools such as changelog generators.
- Helps communicate the intent and scope of changes to teammates and other stakeholders.
- Supports semantic versioning by classifying the nature of changes.
