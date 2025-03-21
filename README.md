# asdf-mcp-plugin

[Model Context Protocol (MCP)](https://github.com/username/mcp) plugin for the [asdf version manager](https://asdf-vm.com).

## Contents

- [Dependencies](#dependencies)
- [Install](#install)
- [Why?](#why)
- [Usage](#usage)
- [Supported MCP Servers](#supported-mcp-servers)
- [Contributing](#contributing)
- [License](#license)

## Dependencies

- `bash`, `curl`, `tar`, `jq`: generic POSIX utilities.

## Install

Plugin:

```shell
asdf plugin add mcp https://github.com/hongsw/asdf-mcp-plugin.git
```

mcp servers:

```shell
# Show all installable versions
asdf list-all mcp

# Install specific version
asdf install mcp latest

# Set a version globally (on your ~/.tool-versions file)
asdf global mcp latest

# Now mcp commands are available
mcp --version
```

Check [asdf](https://github.com/asdf-vm/asdf) readme for more instructions on how to
install & manage versions.

## Why?

The MCP (Model Context Protocol) plugin for asdf simplifies the installation and management of various MCP-compatible servers. It provides a uniform interface for installing, switching between, and managing different versions of MCP servers, eliminating the complexity of manual installation processes for each server type.

## Usage

```shell
# List all available MCP server types
asdf mcp list-servers

# Install a specific MCP server
asdf mcp install <server-name> <version>

# Set a specific MCP server as active
asdf mcp use <server-name> <version>

# Start an MCP server
asdf mcp start <server-name>

# Check status of running MCP servers
asdf mcp status
```

## Supported MCP Servers

This plugin currently supports the following MCP-compatible servers:

- `claude-server`: Anthropic's Claude API compatible server
- `mcp-core`: Reference implementation of the MCP protocol
- `local-llm`: For running local language models with MCP compatibility
- `custom-mcp`: For custom MCP server implementations

## Contributing

Contributions of any kind welcome!

## License

MIT © [hongsw](https://github.com/hongsw/)
