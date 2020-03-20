# Run Pascal script action
![Dockerfile Lint](https://github.com/fabasoad/pascal-action/workflows/Dockerfile%20Lint/badge.svg) ![Shell Lint](https://github.com/fabasoad/pascal-action/workflows/Shell%20Lint/badge.svg) [GitHub release (latest SemVer including pre-releases)](https://img.shields.io/github/v/release/fabasoad/pascal-action?include_prereleases)

This action runs Pascal script.

## Inputs
1. `path` - _[Required]_ Path to the script file.

## Outputs
1. `result` - script output.

## Example usage

### Workflow configuration

```yaml
name: Pascal

on: push

jobs:
  pascal:
    name: Run Pascal script
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v1
      - uses: fabasoad/pascal-action@v1.0.0
        id: pascal
        with:
          path: './HelloWorld.pas'
      - name: Print result
        run: echo "${{ steps.pascal.outputs.result }}"
```

### Result
![Result](https://raw.githubusercontent.com/fabasoad/pascal-action/master/screenshot.png)