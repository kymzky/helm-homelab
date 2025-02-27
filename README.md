# helm-homelab

A collection of Helm charts used in my homelab. These charts are for
applications that do not have an official Helm chart or for my own software.

## Usage

Add this repository to Helm and install charts as needed:

```sh
helm repo add homelab https://kymzky.github.io/helm-homelab
helm install my-release homelab/<chart>
```

For more detailed examples, see my [argocd-homelab](https://github.com/kymzky/argocd-homelab)
repository.

### Add/update chart

To add a Helm chart to this repository or to updated an existing one follow
these steps:

1. Add/modify the new chart in the [charts](./charts/) directory
2. Check [Releases](https://github.com/kymzky/helm-homelab/releases) to ensure that the new release does not exist yet
3. Commit and push changes to the main branch to trigger the chart release (see [release.yaml](./.github/workflows/release.yaml))
4. Check if Renovate's [Dependency Dashboard](https://github.com/kymzky/helm-homelab/issues/4)
has correctly identified all dependencies and versions (customize [renovate.json](./renovate.json)
if not)
5. Update [README.md](./README.md)
