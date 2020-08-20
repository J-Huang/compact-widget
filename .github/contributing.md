# Contributing

This document intends to serve as a reference for developers seeking to develop
& submit pull requests (PRs) to this repository.

## Overview

Our change process is similar to most open-source change models, with some
unique constraints. Generally, you will want to:

- Clone `<this-repo>`
- `git checkout <branchname>`. We have no constraints on branchname.
- We **strongly** recommend [reviewing our onboarding guide](../docs/index.md).
- Update the library or application as seen fit. See individual libraries in
  `lib/*` or applications in `apps/*` for specific instructions on how to
  develop against them.
- Add tests, of course :).
- Open a pull request, and **fill out the template**.
- Await adequate approval. Approval requirements are tracked in
  [git-conventions.md](../docs/git-conventions.md).
- Ask a bot to merge your PR. instructions are captured in the PR template! ex:
  `@probot-buddy merge`
- Celebrate :tada:. Thank you for your contribution.

## PR Description

The PR description requirements are captured in the PR template presented to you
on creation. Regardless, the developer should submit the PR with a title and a
description. The title should include a one-line summary of the PR and the JIRA
ticket number it closes. The title must adhere to our
[git conventions](../docs/git-conventions.md)--make sure to read through the
document before you setup your PR.

The description should include an overview of the changes, JIRA tickets/Github
Issues and screenshots of any visual changes.

## Code Review

### Dependencies

Any PR bringing in a 3rd party dependency should answer the following questions
in the description:

- What is the library?
- Why is it needed?
- What is the bundle size for the library? Check on
  [Bundlephobia](https://bundlephobia.com/) for enhanced metrics.
- Have other alternatives been explored i.e lightweight options or writing the
  functionality in-house?

### TypeScript

The PR should adhere to clean code guidelines.

[Clean Code TypeScript](https://github.com/labs42io/clean-code-typescript)

Some of the key aspects to focus on are:

1. Meaningful Variable Names, no Hungarian Notation.
2. Short Functions
3. Functions with 1 or 2 arguments
4. Removing Duplicate Code
   ([Use AHA programming](https://kentcdodds.com/blog/aha-programming))
5. Avoiding double negatives
6. SOLID principles
7. No commented out code

## PR Checks

Before the PR review, the developer should ensure that it passes the following
checks:

- Lint passes and eslint is not disabled.
- The PR includes unit tests (if adding functionality), and all unit tests pass.
- All functional tests pass. If CI fails due to system failures in the CI
  pipeline, the developer should run `npm run test:ci` to validate the tests
  locally and attach a screenshot of the passing tests.

## Review Process

Once the PR is ready for review, the developer should post the PR link on the
Slack channel `#walmart-web` and ping reviewers for review.
