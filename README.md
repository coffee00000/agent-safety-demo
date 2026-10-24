# Agent Safety Demo

A deliberately unsafe repo for testing [Agent Safety Check](https://agent-safety-check-fawn.vercel.app).

Every "secret" here is fake and works nowhere. The files show agent setup mistakes the scanner should flag:

| File | Mistake |
| --- | --- |
| `.mcp.json` | A token written straight into an MCP server's `env` block |
| `.cursor/mcp.json` | A token passed as a command-line argument, and one in a server URL |
| `.claude/settings.json` | Lets the agent run any shell command, skips every permission prompt, and trusts every project MCP server |
| `.claude/settings.local.json` | Personal settings that shouldn't be committed |
| `.env` | An environment file committed to the repo |

Don't copy any of these settings into a real project.
