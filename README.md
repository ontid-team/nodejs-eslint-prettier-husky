# Eslint Prettier Husky template for NodeJs

[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](http://prettier.io) [![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/) [![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)

## Notes

### 1. Why is my git pre-commit hook not executable by default?

- Because files are not executable by default; they must be set to be executable.

```
  chmod ug+x .husky/*
  chmod ug+x .git/hooks/*
```

### 2. Git commit

```shell
  npm run commit
```

### 3. Project release

```shell
  npm run release:patch // Patch release 0.1.0 -> 0.1.1
  npm run release:minor // Minor release 0.1.1 -> 0.2.0
  npm run release:major // Major release 0.2.0 -> 1.0.0
```

### 4. Project Structure

| Name                   | Description                                              |
|------------------------|----------------------------------------------------------|
| **src/**               | Source files                                             |
| **src/config/**        | Application configuration                                |
| **src/core/**          |                                                          |
| **src/db/**            | DB connect, migration, seed and etc.                     |
| **src/decorators/**    |                                                          |
| **src/helpers/**       |                                                          |
| **src/libs/**          | Library source code like a logger, schema, i18n and etc. |
| **src/middleware/**    | Contains all the middleware that we need                 |
| **src/modules/**       |                                                          |
| **src/providers/**     |                                                          |
| **src/templates/**     |                                                          |
| **src/utility-types/** |                                                          |
| **src/utils/**         | Common functions that would be used repetitively         |
| **dist/**              | Compiled source files will be placed here                |
| **tests/**             | Test cases will be placed here                           |
| **tests/unit/**        | Unit Test cases will be placed here                      |
| **tests/integration/** | API routes (Integration) Test cases will be placed here  |

### 5. PullRequest

  - [ ] This PR implements new feature, fix bug, or some other changes
  - [ ] If PR is not ready to review mark it as Draft
  - [ ] All commits in this PR should be by [conventional-commits](https://www.conventionalcommits.org/en/v1.0.0/)
  - [ ] Title of the PR should have issue(s) identifier(s) ("BOX-123 Example title of PR")

### 6. [Production Best Practices: Security](https://expressjs.com/en/advanced/best-practice-security.html)

- Don’t use deprecated or vulnerable versions of Express
- Use TLS
- Use Helmet
- Use cookies securely
- Prevent brute-force attacks against authorization
- Ensure your dependencies are secure
- Avoid other known vulnerabilities
- Additional considerations
