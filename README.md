github-action-build
======

Composite GitHub Action to build a brdgm.me application.

Usage example:

```yaml
name: Build

on:
  push:
    branches-ignore:
      - experimental/**
      - master
  pull_request:
    branches-ignore:
      - experimental/**
      - master
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: brdgm/github-action-build@v1
        with:
          sonar-token: ${{ secrets.SONARCLOUD_TOKEN }}
          github-token: ${{ secrets.GITHUB_TOKEN }}
```
