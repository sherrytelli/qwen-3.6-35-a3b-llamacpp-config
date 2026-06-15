# llama.cpp-llm-settings-for-qwen-3.6-35b-a3b

Settings for optimized for RTX5060ti

## Quick Start

Save the following configuration in a file named `llm.sh` and execute it to start the server with optimized settings for RTX5060ti.

```bash
#!/bin/bash

llama-server \
-m path/to/.gguf \
--fit on \
--fit-ctx 128000 \
--fit-target 256 \
-np 1 \
-fa on \
--no-mmap \
--mlock \
-b 2048 \
-ub 2048 \
-ctk q8_0 \
-ctv q8_0 \
--temp 0.6 \
--top-p 0.95 \
--top-k 20 \
--min-p 0.0 \
--presence-penalty 0.0 \
--repeat-penalty 1.0 \
--reasoning-budget -1 \
--chat-template-kwargs "{\"preserve_thinking\": true}" \
--webui-mcp-proxy \
--host 0.0.0.0

```
to run `llm.sh` execute the following commands in terminal

```bash
bash llm.sh
```
