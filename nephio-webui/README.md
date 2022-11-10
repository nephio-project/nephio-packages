# nephio-webui

## Description
Package for the Nephio Web UI.

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] nephio-webui`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree nephio-webui`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init nephio-webui
kpt live apply nephio-webui --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
