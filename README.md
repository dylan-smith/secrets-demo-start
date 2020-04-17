# Demo GHAS 

## Code Scanning Alerts & Dependency Alerts on non-default Branches

This repo is a copy of the [Apache ActiveMQ repo](https://github.com/apache/activemq).

It was used it due to the amount of vulnerabilities it displays once CodeQL Action perform its scans.

#### :rotating_light: Do not use it to demo features not related to GHAS Code Scanning and Vulnerabilities alerts on non-default branches

## How to use it
<wait for it>

#### `codeql.yml`
Workflow with the CodeQL analysis. Runs at 0:00 UTC on Sunday.

You can check the results of its runs on the [Security Tab](https://github.com/octodemo/demo-vulnerabilities-ghas/security/code-scanning).

#### `dependencies.yml`
Workflow that checks every new PR that changes dependencies files. If the PR introduces dependencies with known vulnerabilities, it fails. PRs that don't change dependencies are not checked.

Uses [this Action](https://github.com/marketplace/actions/scan-a-pr-for-vulnerable-dependencies) to perform the analysis on non-default branches. The Action uses GitHub's [SecurityVulnerability API](https://developer.github.com/v4/object/securityvulnerability/)
