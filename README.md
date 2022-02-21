# action-major-release

[![GitHub release](https://img.shields.io/github/release/Naereen/StrapDown.js.svg)](https://GitHub.com/Naereen/StrapDown.js/releases/)
[![GitHub latest commit](https://badgen.net/github/last-commit/Naereen/Strapdown.js)](https://GitHub.com/Naereen/StrapDown.js/commit/)
[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)
![Release](https://github.com/open-turo/action-major-release/actions/workflows/release.yaml/badge.svg)

GitHub Action: creates a floating branch for the major release

### Inputs

| Input Parameter | Required | Description                                                                                  |
| :-------------: | :------: | -------------------------------------------------------------------------------------------- |
|  major-version  |   true   | The major version (eg. 1, 2, 3). A floating branch of `v<major>` will be created or updated. |
|     dry-run     |  false   | If true - no branch will be created or pushed.                                               |

## Usage

This will create or update a floating branch for the major release.

```yaml
steps:
  - name: Checkout
    uses: actions/checkout@v2
  - name: Action Lint
    uses: open-turo/action-major-release@v1
    with:
      major-version: 1
```
