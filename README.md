# ask

A minimal Bash CLI tool that sends prompts to any OpenAI-compatible LLM API.

## Dependencies

- `curl`
- `jq`

## Setup

```bash
export ASK_API_URL="https://api.groq.com/openai/v1/chat/completions"
export ASK_MODEL="llama-3.3-70b-versatile"
export ASK_API_KEY="your_api_key_here"
chmod +x ask
```

## Usage Examples

```bash
# Simple question
ask "What is the capital of France?"

# Multiple arguments are joined into one prompt
ask "Establishment dates of" "Turkey" "Azerbaijan" "Japan"

# Pipe input
cat script.sh | ask "Explain what this Bash script does:"

# Combine piped input with arguments
./ask "explain this shell command output:" "$(uname -a)"

# Alias example
alias ask-fix="./ask 'Correct any grammatical errors in the input text. Input text:'"
ask-fix "Rhythim is gonna get you"
```

## Known Limitations

- No conversation history; each call is stateless (single-turn only).
- Requires both `curl` and `jq` to be installed.
- Does not support streaming output.
- No timeout handling; hangs if the API is unresponsive.