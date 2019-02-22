# quay.io/intellihr/whalebrew-golang:1.11.5

FROM golang:1.11.5-alpine AS builder

RUN apk --no-cache add curl git make
RUN curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh

RUN go get -u golang.org/x/lint/golint \
  golang.org/x/tools/cmd/goimports \
  github.com/sanity-io/litter \
  github.com/bradleyjkemp/cupaloy \
  github.com/d4l3k/go-pry \
  github.com/motemen/gore
