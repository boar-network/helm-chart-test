# helm-chart-test

This is example repository for testing Helm chart release.


## Example flow


```bash
# add repository
helm repo add helm-chart-test https://boar-network.github.io/helm-chart-test/

# view charts
helm search repo helm-chart-test

# show all information of the chart
helm show all helm-chart-test/http-echo

# render templates with release name = my-test-app
helm template my-test-app helm-chart-test/http-echo

# install chart
# add --dry-run to output all generated chart manifests instead of installing
helm upgrade --install my-test-app helm-chart-test/http-echo --version 0.0.2 --namespace tests
```
