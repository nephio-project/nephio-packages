# nephio-webui

## Description
Package for the Nephio Web UI.

## Usage

### Pre-provision a Secret for OAuth 2.0
When you get this package, the namespace will automatically be set to the same
as the local directory to which you clone the package, typically `nephio-webui`
if you use the commands below. In order for the Web UI to run, you must
provision a Secret with the OAuth 2.0 Client ID and Client Secret.

```
kubectl create ns nephio-webui
kubectl create secret generic -n nephio-webui cad-google-oauth-client --from-literal=client-id=CLIENT_ID_PLACEHOLDER --from-literal=client-secret=CLIENT_SECRET_PLACEHOLDER
```

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
