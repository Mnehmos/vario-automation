# MSHA Compliance Assistant

RAG search API for MSHA mine safety regulations and compliance guidance

## Stats

- Chunks: 545
- Vectors: 545
- Embedding Model: openai/text-embedding-3-small

## Deploy to Railway

1. Push to GitHub
2. Connect repo to Railway
3. Deploy

## MCP Server

Connect via MCP:
```json
{
  "mcpServers": {
    "msha-rag-server": {
      "url": "https://your-railway-url.railway.app/mcp"
    }
  }
}
```

## HTTP Endpoints

- `GET /health` - Health check
- `POST /search` - Search vectors
  ```json
  {
    "query": "your search query",
    "mode": "hybrid",
    "top_k": 10
  }
  ```
