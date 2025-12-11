# Required API Keys Summary

## 🔑 Required Keys for This Project

### 1. OPENAI_API_KEY ⚠️ REQUIRED
- **What it's for**: LLM models (gpt-4o) and embeddings (text-embedding-3-small)
- **Where to get it**: https://platform.openai.com/api-keys
- **Cost**: Pay-per-use (check OpenAI pricing)
- **Status**: ❌ Not set - **YOU MUST ADD THIS**

### 2. TAVILY_API_KEY ⚠️ REQUIRED  
- **What it's for**: External web search when internal knowledge is insufficient
- **Where to get it**: https://tavily.com/
- **Cost**: Free tier available, then pay-per-use
- **Status**: ❌ Not set - **YOU MUST ADD THIS**

### 3. LANGCHAIN_API_KEY (Optional)
- **What it's for**: Tracing and debugging with LangSmith
- **Where to get it**: https://smith.langchain.com/
- **Cost**: Free tier available
- **Status**: ⚪ Optional - not required to run the project

## 📝 How to Set Up

1. Open the file: `src/backend/.env`
2. Replace the empty values with your actual API keys:
   ```
   OPENAI_API_KEY=sk-your-actual-key-here
   TAVILY_API_KEY=tvly-your-actual-key-here
   ```
3. Save the file
4. Run the project: `langgraph dev --no-browser`

## ⚠️ Current Error

The project cannot start because `OPENAI_API_KEY` is not set. The code tries to initialize embeddings at import time, which requires the API key.

**Solution**: Add your OpenAI API key to `src/backend/.env` file.

