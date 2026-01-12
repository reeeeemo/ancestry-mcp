> This server is DEPRICATED - Used a 2024-11-26 snapshot of [MCP](https://github.com/modelcontextprotocol/python-sdk)

# Ancestry MCP Server
[![smithery badge](https://smithery.ai/badge/mcp-server-ancestry)](https://smithery.ai/server/mcp-server-ancestry)
[![MIT licensed][mit-badge]][mit-url]
[![Python Version][python-badge]][python-url]
[![PyPI version][pypi-badge]][pypi-url]

[mit-badge]: https://img.shields.io/pypi/l/mcp.svg
[mit-url]: https://github.com/reeeeemo/ancestry-mcp/blob/main/LICENSE
[python-badge]: https://img.shields.io/pypi/pyversions/mcp.svg
[python-url]: https://www.python.org/downloads/
[pypi-badge]: https://badge.fury.io/py/mcp-server-ancestry.svg
[pypi-url]: https://pypi.org/project/mcp-server-ancestry

Built on top of the [Model Context Protocol Python SDK](https://modelcontextprotocol.io)

<a href="https://glama.ai/mcp/servers/pk5j4bp5nv"><img width="380" height="200" src="https://glama.ai/mcp/servers/pk5j4bp5nv/badge" alt="Ancestry MCP server" /></a>

## Overview

Python server implementing Model Context Protocol (MCP) for interactibility with `.ged` files *(GEDCOM files, commonly seen on Ancestry.com)*

## Features
    
- Read and parse .ged files
- Rename `.ged` files
- Search within .ged files for certain individuals, family, etc

**Note:** The server will only allow operations within the directory specified via `args`

## Resources

- `gedcom://{file_name}`: `.ged` operations interface

## Tools

- **list_files**
    - List a (or multiple) `.ged` file within the directory
    - Input: `name` (string)

- **rename_file**
    - Renames a (or multiple) `.ged` file within the directory
    - Inputs:
        - `file_name` (string): Old file name
        - `new_name` (string)
 
- **view_file**
    - Parses and reads full contents of a `.ged` file
    - Can also parse and read multiple files
    - Can get specific information out of file(s), such as date of birth, marriage, etc.
    - Input: `name` (string)


## Usage with Claude Desktop

### Installing via Smithery

To install Ancestry GEDCOM Server for Claude Desktop automatically via [Smithery](https://smithery.ai/server/mcp-server-ancestry):

```bash
npx -y @smithery/cli install mcp-server-ancestry --client claude
```

### Installing Manually
1. First, install the package:
```pip install mcp-server-ancestry```


2. Add this to your `claude_desktop_config.json` 

```json
{
  "mcpServers": {
     "ancestry": {
       "command": "mcp-server-ancestry",
       "args": ["--gedcom-path", "path/to/your/gedcom/files"]
     }
  }
}
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.
