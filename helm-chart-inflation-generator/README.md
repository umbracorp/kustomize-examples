# Helm Chart Inflation Generator

To build the manifest:
```bash
kubectl kustomize --enable-helm .
```

Note that Kustomize does not support OCI registries.
```yaml
apiVersion: builtin
kind: HelmChartInflationGenerator
metadata:
  name: dokuwiki-helm
name: dokuwiki
repo: oci://registry-1.docker.io/bitnamicharts/  # won't work
version: 14.3.2
releaseName: dokuwiki
namespace: test
# valuesFile: values.yaml
IncludeCRDs: true
```