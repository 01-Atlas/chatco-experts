# Chat.co experts

Pre-release package for connecting Chat.co experts to supported external AI clients. The shared service is under development; this package has not been submitted or published to a marketplace, and the production endpoint is not yet launch-ready.

The intended experience is to sign in to Chat.co, select a workspace, ask an expert, and receive an answer with citations and supporting-document links. Direct document search is available only when your Chat.co permissions allow it.

## Connection

The planned remote MCP URL is `https://mcp.chat.co/mcp`. Use the client's OAuth sign-in flow. Do not put an API key or another person's login into these configuration files.

Cursor discovers `.cursor-plugin/plugin.json` and `mcp.json`. Claude Code discovers `.claude-plugin/plugin.json` and `.mcp.json`. Grok Build packaging uses `.grok-plugin/plugin.json`, `.mcp.json`, and the shared skill. Marketplace acceptance and compatibility with each client are verified separately before release.

## Costs and access

- An expert answer uses that expert's normal Chat.co message rate.
- A completed standalone document search uses 0.5 message credit. Internal retrieval for an expert answer is included in its message rate.
- Listing experts and reading returned evidence are free.
- Permissions, licenses, document deletion, and your selected billing context still apply.

## Privacy

Your external AI client sends your request to Chat.co and receives the resulting answer, permitted excerpts, citations, and links. Its handling of that content is governed by that client's policies. Disconnecting stops future connector access; it cannot retract content already delivered.

## Package boundary

This directory is the publishable package. It contains manifests, configuration, a skill, and Chat.co artwork. The application backend, infrastructure credentials, customer documents, and reviewer credentials must remain outside the public package. MIT applies to the package files; Chat.co names and marks remain the property of their owners.
