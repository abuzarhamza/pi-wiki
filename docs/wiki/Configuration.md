# Configuration

## Gemini Key
To use Gemini with Pi, you need to set your API key.
Set the `GEMINI_API_KEY` environment variable:
```bash
export GEMINI_API_KEY=your_api_key_here
```

## Model Selection
You can configure which model Pi uses in your configuration file (usually in `~/.pi/config.json`).
Set the `model` field to `gemini-pro` or another supported model.
