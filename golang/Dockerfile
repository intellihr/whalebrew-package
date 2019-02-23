# quay.io/intellihr/whalebrew-golang:1.11.5

FROM golang:1.11.5-alpine AS builder

RUN apk --no-cache add curl git make
RUN curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh

RUN go get -u golang.org/x/lint/golint \
  github.com/acroca/go-symbols \
  github.com/bradleyjkemp/cupaloy \
  github.com/d4l3k/go-pry \
  github.com/go-delve/delve/cmd/dlv \
  github.com/mdempsky/gocode \
  github.com/motemen/gore \
  github.com/ramya-rao-a/go-outline \
  github.com/rogpeppe/godef \
  github.com/sanity-io/litter \
  github.com/sqs/goreturns \
  github.com/uudashr/gopkgs/cmd/gopkgs \
  github.com/zmb3/gogetdoc \
  golang.org/x/tools/cmd/godoc \
  golang.org/x/tools/cmd/goimports \
  golang.org/x/tools/cmd/gorename \
  golang.org/x/tools/cmd/guru

WORKDIR /workdir

# This is a special hack to make vscode editor work
RUN mkdir -p /vendor && chmod -R 777 /vendor && \
    mkdir -p /.cache && chmod -R 777 /.cache
ENV CGO_ENABLED=0
ENV GOPATH=/go:/vendor
LABEL io.whalebrew.config.volumes '["${PWD}/vendor:/vendor/src"]'

ENTRYPOINT ["go"]
