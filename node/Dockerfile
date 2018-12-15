# quay.io/intellihr/whalebrew-node:8.14

FROM node:8.14-alpine

RUN npm install tslint typescript -g && \
    apk update && apk upgrade && \
    apk add --no-cache bash git openssh

ENTRYPOINT ["node"]
