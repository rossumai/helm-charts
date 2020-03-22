# Update a Helm chart

To update or add a chart, create a directory with new chart tarball(s) and run:

```shell
HELM_CHARTS_REPO=<PATH_TO_HELM_CHARTS_REPO>
helm repo index --url https://rossumai.github.io/helm-charts/ --merge $HELM_CHARTS_REPO/index.yaml .
cp  *.tgz index.yaml $HELM_CHARTS_REPO
( cd $HELM_CHARTS_REPO; git add *.tgz index.yaml; git commit -m "New version of ... released"; git push origin master )
```
