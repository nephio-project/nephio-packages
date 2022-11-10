# package-deployment-controller

## Description
package-deployment controller

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] package-deployment-controller`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree package-deployment-controller`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init package-deployment-controller
kpt live apply package-deployment-controller --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
