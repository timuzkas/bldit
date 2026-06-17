# bldit

Clone a Git repo and have a local LLM (via llama.cpp) explore, build, and optionally install it.

## Requirements

- Python 3.10+
- [llama.cpp](https://github.com/ggml-org/llama.cpp) built with server support on your `PATH`
- `pip install requests`

## Usage

```bash
./bldit <repo-url-or-local-path> [options]
```

## Options

| Flag | Description |
|------|-------------|
| `--ask` | Confirm each tool call before running |
| `--install` | Also install the project after building |
| `--keep` | Keep the temp clone directory |
| `--prompt <text>` | Inject a custom instruction into the LLM prompt |
| `--model <name>` | Model to use (HuggingFace repo:filename) |
| `--url <url>` | OpenAI-compatible API base URL |
| `--api-key <key>` | API key for remote providers |
| `--kill` | Stop any running llama-server |

## Config

Stored at `~/.config/bldit/config.json`. Persistent settings include model name, `prompt_additions`, and `always_allow_tools`.
