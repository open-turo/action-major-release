# `open-turo/action-major-release`

## Description

GitHub Action that conditionally creates a floating branch for a major release. This is best combined with Semantic Release to provide consistent major versioning. See [open-turo/actions-gha](https://github.com/open-turo/actions-gha), which calls this from its `./release` action for example usage.

[![Release](https://img.shields.io/github/v/release/open-turo/action-major-release)](https://github.com/open-turo/action-major-release/releases/)
[![Tests pass/fail](https://img.shields.io/github/workflow/status/open-turo/action-major-release/CI)](https://github.com/open-turo/action-major-release/actions/)
[![License](https://img.shields.io/github/license/open-turo/action-major-release)](./LICENSE)
[![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](https://github.com/dwyl/esta/issues)
![CI](https://github.com/open-turo/action-major-release/actions/workflows/release.yaml/badge.svg)
[![semantic-release: angular](https://img.shields.io/badge/semantic--release-angular-e10079?logo=semantic-release)](https://github.com/semantic-release/semantic-release)
[![Conventional commits](https://img.shields.io/badge/conventional%20commits-1.0.2-%23FE5196?logo=conventionalcommits&logoColor=white)](https://conventionalcommits.org)
[![Join us!](https://img.shields.io/badge/Turo-Join%20us%21-593CFB.svg)](https://turo.com/jobs)

## Usage

### Execute the action to create/update the major release

In this case, a branch will be attempted to be created and pushed.

```yaml
steps:
  - name: Major release
    uses: open-turo/action-major-release@v1
    with:
      major-version: 1
```

### Execute the action in "dry run" mode

In this case, no branch will be created nor pushed. The commands that would be executed if not in dry run mode will be
sent to stdout.

```yaml
steps:
  - name: Major release
    uses: open-turo/action-major-release@v1
    with:
      major-version: 1
      dry-run: true
```

## Inputs

| parameter     | description                                                                                          | required | default |
| ------------- | ---------------------------------------------------------------------------------------------------- | -------- | ------- |
| major-version | The major version to publish. This will update the branch `v<major-version>` to the current git sha. | `true`   |         |
| dry-run       | Whether to run the action in dry-run mode - no branches will be created or pushed.                   | `false`  | false   |

## Runs

This action is an `composite` action.

## Get Help

Please review Issues, post new Issues against this repository as needed.

## Contributions

Please see [here](https://github.com/open-turo/contributions) for guidelines on how to contribute to this project.
