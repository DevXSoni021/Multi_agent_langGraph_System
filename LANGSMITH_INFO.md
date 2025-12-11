# LangSmith API Key - Optional

## Is LangSmith Required?

**No, LangSmith is NOT required** for the system to work. It's completely optional.

## What is LangSmith Used For?

LangSmith is used for:
- **Tracing and debugging** - Visualize the execution flow of your agents
- **Monitoring** - Track performance and usage
- **Observability** - Debug issues in production

## When Do You Need It?

You only need the LangSmith API key if you want to:
- Debug agent execution flows
- Monitor system performance
- Use LangGraph Studio for visualization
- Track API usage and costs

## How to Get LangSmith API Key (Optional)

1. Go to: https://smith.langchain.com/
2. Sign up for a free account
3. Navigate to Settings → API Keys
4. Create a new API key
5. Add it to your `.env` file as `LANGCHAIN_API_KEY`

## Running Without LangSmith

The system works perfectly fine without LangSmith. You'll just see a warning message:
```
LangSmithMissingAPIKeyWarning: API key must be provided when using hosted LangSmith API
```

This warning can be safely ignored. The system will function normally.

## Current Configuration

In `src/backend/config.py`, LangSmith settings are:
- `LANGCHAIN_API_KEY`: Optional (empty string by default)
- `LANGCHAIN_TRACING_V2`: Set to `true` (but won't work without API key)
- `LANGCHAIN_PROJECT_NAME`: "multi_agent_system"

You can disable tracing by setting `LANGCHAIN_TRACING_V2=false` in your `.env` file if you don't want the warning.

