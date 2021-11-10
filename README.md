
TETRATE_GOLANG_SDK_DIR=~/projects/src/github.com/tetratelabs/proxy-wasm-go-sdk

 docker run --workdir /tmp/proxy-wasm-go --volume $PWD:/tmp/proxy-wasm-go --volume $TETRATE_GOLANG_SDK_DIR/proxywasm:/tmp/proxy-wasm-go/proxywasm tinygo/tinygo:0.20.0   tinygo build -o /tmp/proxy-wasm-go/main.go.wasm -scheduler=none -target=wasi /tmp/proxy-wasm-go/main.go