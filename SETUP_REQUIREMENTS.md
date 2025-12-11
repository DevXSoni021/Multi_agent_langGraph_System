# Setup Requirements

## Required API Keys

This project requires the following API keys to be set in your environment:

### 1. OPENAI_API_KEY (Required)
- **Purpose**: Used for LLM access and embeddings
- **Where to get it**: https://platform.openai.com/api-keys
- **Usage**: Powers the chat models (gpt-4o) and embedding models (text-embedding-3-small)

### 2. TAVILY_API_KEY (Required)
- **Purpose**: Used for external web search by the Knowledge Agent
- **Where to get it**: https://tavily.com/
- **Usage**: Enables the system to search the web when internal knowledge is insufficient

### 3. LANGCHAIN_API_KEY (Optional)
- **Purpose**: For tracing and debugging with LangSmith
- **Where to get it**: https://smith.langchain.com/
- **Usage**: Enables observability and debugging of the LangGraph execution

## Environment Setup

Create a `.env` file in `src/backend/` directory with the following format:

```env
# Required
OPENAI_API_KEY=your_openai_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here

# Optional (for LangSmith tracing)
LANGCHAIN_API_KEY=your_langchain_api_key_here
LANGCHAIN_ENDPOINT=https://api.smith.langchain.com
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT_NAME=multi_agent_system
```

## Python Version Requirement

**IMPORTANT**: This project requires Python >= 3.11

✅ **Status**: Python 3.11.14 has been installed using `uv python install 3.11`

## Installation Steps

✅ **Completed Steps**:
1. ✅ Installed `uv` package manager
2. ✅ Installed Python 3.11.14 using `uv python install 3.11`
3. ✅ Created virtual environment with Python 3.11
4. ✅ Installed all project dependencies
5. ✅ Installed `langgraph-cli` (version 0.4.9)
6. ✅ Created `.env` file template at `src/backend/.env`

## Current Status

⚠️ **Action Required**: You need to add your API keys to the `.env` file before running the project.

The `.env` file is located at: `src/backend/.env`

Edit this file and add your actual API keys:
```bash
nano src/backend/.env
# or
vim src/backend/.env
# or open in your editor
```

## Running the Application

Once you've added your API keys to `src/backend/.env`, run:

```bash
cd /Users/devashishsoni/Downloads/multi_agent_system
export PATH="$HOME/.local/bin:$PATH"
source .venv/bin/activate
langgraph dev --no-browser
```

The application will be available at `http://127.0.0.1:2024`

## Error Resolution

If you encounter errors:

1. **"OPENAI_API_KEY not set"**: Make sure you've added your OpenAI API key to `src/backend/.env`
2. **"TAVILY_API_KEY not set"**: Make sure you've added your Tavily API key to `src/backend/.env`
3. **Import errors**: Make sure the virtual environment is activated: `source .venv/bin/activate`
4. **LangGraph CLI not found**: Make sure `langgraph-cli` is installed in the virtual environment

