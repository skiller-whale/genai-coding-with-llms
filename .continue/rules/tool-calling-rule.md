---
name: Tool Calling Rule
alwaysApply: true
description: Tool calling rules (MCP)
---

If using the tool `execute_command`, OUTPUT THE COMMAND BEFORE YOU CALL THE TOOL.

Example:
    [input]
        Run `ls -a`.
    [input]

    [assistant]
        **Command**: `ls -a`
        <execute_command tool call>
    [assistant]
