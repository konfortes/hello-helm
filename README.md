# hello-helm

This is a sample repo with chart generated with the `helm create` command to run nginx:latest.  
It is used as a Helm repo using Github pages.

## Package the chart

```bash
helm package source-charts/*
```

## Index

```bash
helm repo index --url https://konfortes.github.io/hello-helm/ .
```
