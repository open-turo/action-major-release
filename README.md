# `open-turo/action-major-release`

<!-- prettier-ignore-start -->
<!-- action-docs-description source="action.yaml" -->
## Description

GitHub Action that conditionally creates a floating branch for a major release
<!-- action-docs-description source="action.yaml" -->
<!-- prettier-ignore-end -->

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

<!-- prettier-ignore-start -->
<!-- action-docs-inputs source="action.yaml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `major-version` | <p>The major version to publish. This will update the branch <code>v&lt;major-version&gt;</code> to the current git sha.</p> | `true` | `""` |
| `dry-run` | <p>Whether to run the action in dry-run mode - no branches will be created or pushed.</p> | `false` | `false` |
<!-- action-docs-inputs source="action.yaml" -->
<!-- action-docs-outputs source="action.yaml" -->

<!-- action-docs-outputs source="action.yaml" -->
<!-- action-docs-runs source="action.yaml" -->
## Runs

This action is a `composite` action.
<!-- action-docs-runs source="action.yaml" -->
<!-- action-docs-usage source="action.yaml"  -->
<!-- prettier-ignore-end -->
