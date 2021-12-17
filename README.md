js:
protoc --proto_path=. --js_out=import_style=commonjs,binary:build/js schemas/*.proto

ts:
# install protoc ts plugin:
# npm install -g ts-protoc-gen
protoc --proto_path=. --ts_out=build/js schemas/*.proto

rs:
# install protoc rust plugin:
# cargo install protobuf-codegen
protoc --rust_out build/rs schemas/*.proto

cargo package --allow-dirty
