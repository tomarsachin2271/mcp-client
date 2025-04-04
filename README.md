# MCP Client TypeScript

A TypeScript implementation of a Model Context Protocol (MCP) client that integrates with Anthropic's Claude API. This client enables interaction with MCP-compatible servers and provides a command-line interface for sending queries.

## Features

- Seamless integration with Anthropic's Claude API
- Support for both JavaScript and Python MCP servers
- Interactive command-line interface
- Dynamic tool loading from MCP servers
- Cross-platform compatibility

## Prerequisites

- Node.js (Latest LTS version recommended)
- TypeScript
- An Anthropic API key

## Installation

1. Clone the repository:
```bash
git clone https://github.com/tomarsachin2271/mcp-client-typescript.git
cd mcp-client-typescript
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory and add your Anthropic API key:
```env
ANTHROPIC_API_KEY=your_api_key_here
```

## Dependencies

- `@anthropic-ai/sdk`: Anthropic's official SDK for Claude API integration
- `@modelcontextprotocol/sdk`: Model Context Protocol SDK
- `dotenv`: For environment variable management

## Usage

To start the MCP client, run:

```bash
node index.ts <path_to_server_script>
```

Where `<path_to_server_script>` can be either a JavaScript (.js) or Python (.py) server script.

### Interactive Mode

Once started, the client enters an interactive mode where you can:
1. Type your queries and press Enter to send them
2. Type 'quit' to exit the application

### Features

- **Server Connection**: Automatically connects to the specified MCP server
- **Tool Discovery**: Lists available tools from the connected server
- **Query Processing**: Processes queries using Claude API and executes tool calls
- **Cross-Platform**: Works on both Windows and Unix-based systems

## Implementation Details

The client is implemented in TypeScript and consists of the following main components:

- `MCPClient` class: Main client implementation
  - `connectToServer()`: Establishes connection with MCP server
  - `processQuery()`: Handles query processing and tool execution
  - `chatLoop()`: Manages the interactive command-line interface

## Error Handling

The client includes robust error handling for:
- Missing API keys
- Server connection failures
- Invalid server script paths
- Tool execution errors

## License

MIT License

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. 