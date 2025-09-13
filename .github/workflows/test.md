---
on:
  workflow_dispatch:
  pull_request:
    branches:
      - main

permissions: read-all

network: defaults

safe-outputs:
  push-to-pr-branch:
  create-issue:
    title-prefix: "${{ github.workflow }}"
  add-issue-comment:

tools:
  web-fetch:
  web-search:
  bash: [":*"]
---

# Workflow for Running Code Tests, Linting, and Formatting

Your job is to run tests, linting, and formatting on code submitted to pull requests, make necessary fixes, and reflect the changes to the pull request.
Please execute the task following these steps:

1. Run test, lint, and format commands
2. Check the output and fix any errors
3. Reflect changes to the pull request
4. Repeat steps 1-3 until all tests pass and there are no lint or formatting errors
