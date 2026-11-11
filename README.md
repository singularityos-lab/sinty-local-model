# Sinty Local Model

The model that answers Sinty AI on the computer itself. Nothing it reads or
writes leaves the machine.

It is an SXI application. Once installed it starts with the session and serves
an OpenAI compatible API on `127.0.0.1:11435`, which is where the `local`
provider of `sinty` looks by default.

The first start downloads [Qwen3 4B](https://huggingface.co/Qwen/Qwen3-4B-GGUF)
(Q4_K_M, 2.5 GB, Apache-2.0) into `~/.local/share/sinty-local-model` and checks
its SHA-256 before using it. Set `SINTY_LOCAL_MODEL` to the path of another GGUF
file to use a different model.

The server is [llama.cpp](https://github.com/ggml-org/llama.cpp), built by the
workflow in this repository for x86_64 and aarch64 against glibc 2.42.

## License

The scripts are GPL-3.0-or-later. llama.cpp is MIT.
