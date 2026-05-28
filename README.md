# ytsum

Extract YouTube transcript & summarize with AI.

## Install

```bash
sudo apt install -y jq curl yt-dlp
```

```bash
curl -L https://raw.githubusercontent.com/rizmulya/ytsum/main/ytsum -o ytsum && \
chmod +x ytsum && \
sudo mv ytsum /usr/local/bin/
```

## API Key

DeepSeek:

```bash
export DEEPSEEK_API_KEY="your_key"
```

OpenAI:

```bash
export OPENAI_API_KEY="your_key"
```

## Usage

```bash
ytsum -u <youtube_url> [options]
```

```bash
Options:
  -u, --url         YouTube URL
  -l, --lang        Subtitle language (default: en)

  -s, --summarize   Summarize language
                    Example:
                      -s english
                      -s indonesia

  -p, --provider    AI provider:
                      deepseek
                      openai
                    (default: deepseek)
```

```bash
Examples:
  ytsum -u URL
  ytsum -u URL -l id
  ytsum -u URL -s english
  ytsum -u URL -s indonesia -p openai
```

## Output

- `[title].txt` - Clean transcript
- `Summary_[title].md` - AI-generated summary (when using -s)
