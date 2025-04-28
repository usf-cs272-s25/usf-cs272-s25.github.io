---
layout: assignment
due: 2025-05-06 23:59:59 -0700
github_url: https://classroom.github.com/a/Ox4JSVGT
published: false
---

## Background

1. We have developed several Tools using the OpenAI tool-calling APIs
1. In order to be really useful, tools need to be callable from a variety of chat clients,
rather than trapped in a chat client of our own design
1. The [Model Context Protocol](https://modelcontextprotocol.io/introduction) (MCP) is designed to bridge this gap
1. MCP enables public collections of MCP Servers (tools) like [MCP Server Hub](https://mcpserverhub.com/) and others


## Requirements

1. You will incorporate your course catalog tool and the second tool you built for project06
1. You will make those tools available using the MCP Transport of your choice
1. You will incorporate your tools into [Claude Desktop](https://claude.ai/download) (ChatGPT Desktop does not yet support MCP)

## Given

1. We will discuss MCP in lecture
1. Several implementations of MCP are available for Go ([metoro-io](https://github.com/metoro-io/mcp-golang/tree/main), [mark3labs](https://github.com/mark3labs/mcp-go), perhaps others)
1. You may decide how much of the code to write by hand vs. using Cursor or other AI coding assistant


## Rubric

1. 50 points - Demonstrate your course catalog tool from Claude Desktop
1. 30 points - Demonstrate your second tool from Claude Desktop
1. 20 points - Partner code review in class
    1. 5 points - No binaries in the repo
    1. 5 points - No commented-out (dead) code
    1. 5 points - Reasonable Separation of Concerns (no long main files/functions)
    1. 5 points - Use of object-oriented methods and receivers
    1. 0 points - If you used an AI coding assistant, describe your prompts