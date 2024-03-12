# Blank Petstore

A basic Petstore app and associated OpenAPI spec.

## Build

```bash
# Multiarch with buildx
docker buildx create --name mybuilder --use

docker buildx inspect --bootstrap

docker buildx build --platform linux/amd64,linux/arm64 -t quay.io/kuadrant/blank-petstore:1.0.x --push .
```

### Local build
```bash
docker buildx build --load --platform linux/arm64 -t quay.io/kuadrant/blank-petstore:1.0.x .
```

## Run

```bash
docker run --name blank-petstore -p 8080:8080 quay.io/kuadrant/blank-petstore:1.0.x
```


## OAS Spec

Located Here:

`openapi.yaml`

