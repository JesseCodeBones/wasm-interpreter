
### compile C to wasm command 
`clang --target=wasm32 --no-standard-libraries -Wl,--export-all -Wl,--no-entry -Wl,--allow-undefined  -o helloworld.wasm -I. ./helloworld.c`  
