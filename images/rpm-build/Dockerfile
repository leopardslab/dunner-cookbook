FROM golang:1.11-alpine3.8

RUN apk add --no-cache bash \
                       build-base \
                       curl \
                       git \
                       rpm

RUN go get -u github.com/golang/dep/cmd/dep

WORKDIR /app

ARG GORELEASER_VERSION=v0.112.2

RUN curl -L -o goreleaser.tgz \
      https://github.com/goreleaser/goreleaser/releases/download/${GORELEASER_VERSION}/goreleaser_Linux_x86_64.tar.gz && \
      tar -zxvf goreleaser.tgz -C /usr/local/bin/ && \
      rm -f goreleaser.tgz