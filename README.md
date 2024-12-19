# cognee-mcp-server

An MCP server for [cognee](https://www.cognee.ai/), an AI memory engine.

## Tools

- `Cognify_and_search` : Builds knowledge graph from the input text and performs search in it.
  - Inputs:
    - `text` (String): Context for knowledge graph contstruction
    - `search_query` (String): Query for retrieval
    - `graph_model_file` (String, optional): Filename of a custom pydantic graph model implementation
    - `graph_model_name` (String, optional): Class name of a custom pydantic graph model implementation
  - Output:
    - Retrieved edges of the knowledge graph

## Configuration
### Usage with Claude Desktop

Install uv with homebrew.

Add this to your claude_desktop_config.json:
<details>
<summary>Using uvx</summary>

```
"mcpcognee": {
  "command": "uv",
  "args": [
    "--directory",
    "/path/to/your/cognee-mcp-server",
    "run",
    "mcpcognee"
  ],
  "env": {
    "ENV": "local",
    "TOKENIZERS_PARALLELISM": "false",
    "LLM_API_KEY": “your llm api key”,
    "GRAPH_DATABASE_PROVIDER": “networkx”,
    "VECTOR_DB_PROVIDER": "lancedb",
    "DB_PROVIDER": "sqlite",
    "DB_NAME": “cognee_db”
  }
}
```
</details>
