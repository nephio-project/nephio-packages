# nephio-configsync

## Description
Package for the ConfigSync on Nephio workload clusters.

To use this package in your own environment, you should modify the `repo` field
in the `rootsync.yaml` file to point to your GitHub user. The repo name itself
will be changed during `kpt fn render` to point to the repo with the same name
as the package instance.

Thus, you could clone this package from the upstream Nephio repository, and
modify the `repo` value, then store it in your organizational repository and
consume it from there in the future. This would eliminate any need to customize
package on each instantiation.

This package is also configured for no Git authentication or authorization. See
the Config Sync
[documentation](https://cloud.google.com/anthos-config-management/docs/how-to/installing-config-sync#git-creds-secret)
for details.

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] nephio-configsync`

Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree nephio-configsync`

Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init nephio-configsync
kpt live apply nephio-configsync --reconcile-timeout=2m --output=table
```

Details: https://kpt.dev/reference/cli/live/
