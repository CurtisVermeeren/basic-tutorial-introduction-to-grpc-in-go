# Intoduction to gRPC in Go
Project follows along with the grpc introduction using Go. https://grpc.io/docs/languages/go/

## Quickstart gRPC in Go
Install the Protocol buffer compiler. `apt install -y protobuf-compiler`

Install the Go plugins for the protocol compiler. `go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28` and `go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2`

Update the path so that protoc compiler can find the plugins. `export PATH="$PATH:$(go env GOPATH)/bin"`

Generate gRPC code `protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative helloworld/helloworld.proto` This will generate `helloworld/hellowrld.pb.go` and `helloworld/helloworld_grpc.pb.go` files.

Generate routeguide using `protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative routeguide/route_guide.proto`