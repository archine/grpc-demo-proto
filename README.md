## Grpc DEMO proto file
This repository contains a simple gRPC service definition using Protocol Buffers (proto3 syntax). The service is designed to demonstrate basic gRPC functionality, including defining messages and services.

## 必须：
- Go 1.24 or later
- Protobuf compiler [protoc](https://grpc.io/docs/protoc-installation/)
- Install the gRPC Go plugin:
```bash
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest

go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

## 编译 proto文件
最后的 `hello/hello.proto` 是 proto 文件的路径，根据实际情况修改。
```bash
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative hello/hello.proto
```