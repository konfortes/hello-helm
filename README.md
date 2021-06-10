# hello-helm

This is a sample repo with chart generated with the `helm create` command to run nginx:latest.  
It is used as a Helm repo using Github pages.

## Package the chart

```bash
helm package -d http-service source-charts/http-service
```

## Index

```bash
helm repo index --url https://konfortes.github.io/hello-helm/ .
```

## Configure the Client

```bash
helm repo add konfortes https://konfortes.github.io/hello-helm
```

## Adding More Charts

After packaging:

```bash
helm repo index --url https://konfortes.github.io/hello-helm/ --merge index.yaml .
```

## Consume Charts from This Repo

```bash
helm repo add konfortes https://konfortes.github.io/hello-helm

helm install my-http-service konfortes/http-service
```

## Run Presentation

```bash
cd helm-presentation
slidev -o
```
