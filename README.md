# action-major-release

![][version-image]
![][workflows-badge-image]
[![Release date][release-date-image]][release-url]
[![semantic-release][semantic-image]][semantic-url]

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
