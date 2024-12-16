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
