# docker-basic-buildx

Aplicación básica que permite la ejecución de un proceso cada 5 segundos.

Comandos permitidos
```
npm install
npm run test
npm start
```

# Comandos importantes usados aquí

## BUILDX
[Buildx Referencia](https://docs.docker.com/build/building/multi-platform/#getting-started)

### CMD
```
docker buildx build \
--platform linux/amd64,linux/arm64 \
-t emmartel/cron-ticker --push .
```
### Dockerfile
```
# /app /usr /lib
# FROM --platform=linux/amd64 node:19.2-alpine3.16
# FROM --platform=$BUILDPLATFORM node:19.2-alpine3.16
FROM node:19.2-alpine3.16
```
