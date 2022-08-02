# nephio-system

## Description
Package for the basic Nephio software.

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] nephio-system`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree nephio-system`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init nephio-system
kpt live apply nephio-system --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
