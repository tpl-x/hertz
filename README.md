# herz
## install tool
hz
```bash
go install github.com/cloudwego/hertz/cmd/hz@latest
```
openapi plugin
```bash
go install github.com/google/gnostic/cmd/protoc-gen-openapi@latest
```
init project
```bash
 hz new \       
  -I proto \
  -idl proto/api/v1/hello.proto \
  -mod github.com/tpl-x/hertz \
  -model_dir biz/model \
  -handler_dir biz/handler
  --protoc-plugins=openapi::./docs 
```
update idl
```bash
hz update -I proto \
  -idl proto/api/v1/hello.proto \
  --protoc-plugins=openapi::./docs 
```