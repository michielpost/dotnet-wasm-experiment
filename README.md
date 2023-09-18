# dotnet-wasm-experiment
Experimenting with dotnet wasm

Publish:
```ps
dotnet publish WasiConsoleTest
```

Result is here:
> \WasiConsoleTest\obj\Release\net8.0\wasi-wasm\wasm\for-publish\WasiConsoleTest.wasm``

Optimize:
```ps
wasm-opt -Oz --enable-bulk-memory WasiConsoleTest.wasm -o WasiConsoleTestOpt.wasm 
```

Run:
```
wasmtime WasiConsoleTestOpt.wasm 
```

Result
> Hello, Wasi Console!


## References
- https://www.strathweb.com/2022/12/dotnet-wasi-applications-in-the-cloud/
- https://henrikrxn.github.io/blog/Webassembly-dotnet-8-hello-world/