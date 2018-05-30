FROM golang:alpine AS binary

RUN apk update && apk upgrade && \
    apk add --no-cache git
RUN go get github.com/github/hub

FROM alpine:3.7
LABEL io.whalebrew.name hub

RUN apk update && apk upgrade && \
    apk add --no-cache git
COPY --from=binary /go/bin/hub /usr/local/bin/hub
ENTRYPOINT ["hub"]
