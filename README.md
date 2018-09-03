# Golang World sample docker images example


This is a basic hello world sample for golang showing the image sizes created by various build process.


## Creating docker images

1. Using golang:1.11
    * Building: `docker build . -f Dockerfile-golang-1-11 -t golang-app:golang-1-11`
    * Running: `docker run golang-app:golang-1-11`

2. Using golang:1.11-alpine

    * Building: `docker build . -f Dockerfile-golang-1-11-alpine -t golang-app:golang-1-11-alpine`
    * Running: `docker run golang-app:golang-1-11-alpine`

3. Using multistage build

    * Building: `docker build . -f Dockerfile-golang-1-11-multi-stage -t golang-app:multistage`
    * Running: `docker run golang-app:multistage`


View created docker images: `docker images golang-app`


```
 $ > docker images golang-app
 REPOSITORY          TAG                  IMAGE ID            CREATED             SIZE
 golang-app          multistage           669a33298ed2        9 seconds ago       5.93MB
 golang-app          golang-1-11-alpine   0bf45c1ca890        8 minutes ago       311MB
 golang-app          golang-1-11          4393168f3554        17 minutes ago      776MB
```

Ref: [https://github.com/GoogleCloudPlatform/nodejs-docs-samples](https://github.com/GoogleCloudPlatform/nodejs-docs-samples)
