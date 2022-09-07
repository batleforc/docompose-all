FROM golang:1.19-bullseye

RUN apt update && apt install -y protobuf-compiler

RUN protoc --version

RUN go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
RUN go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
RUN export PATH="$PATH:$(go env GOPATH)/bin"