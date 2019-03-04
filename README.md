# linuxserver/doc-builder

Expects to run as part of the LSIO CI process. Not for public consumption.

**Running against remote: **
```
docker run --rm \
-e CONTAINER_NAME=${CONTAINER_NAME} \
-v ${TEMPDIR}:/ansible/readme \
linuxserver/doc-builder:latest
```
**Running locally: **

If you need to test functionality just navigate to the folder with the readme-vars.yml and run: 
```
docker run --rm \
-v $(pwd):/tmp \
-e LOCAL=true \
linuxserver/doc-builder:latest
```
The output will be in a GENERATED.md in your current working directory.
