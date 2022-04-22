# `open-turo/action-major-release`

## Description

GitHub Action that conditionally creates a floating branch for a major release

[![GitHub release](https://img.shields.io/github/release/Naereen/StrapDown.js.svg)](https://GitHub.com/Naereen/StrapDown.js/releases/)
[![GitHub latest commit](https://badgen.net/github/last-commit/Naereen/Strapdown.js)](https://GitHub.com/Naereen/StrapDown.js/commit/)
[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)
![Release](https://github.com/open-turo/action-major-release/actions/workflows/release.yaml/badge.svg)

## Usage

```yaml
steps:
  - name: Major release
    uses: open-turo/action-major-release@v1
    with:
      major-version: 1
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
