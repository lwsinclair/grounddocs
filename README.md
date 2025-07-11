[![MseeP.ai Security Assessment Badge](https://mseep.net/pr/grounddocs-grounddocs-badge.png)](https://mseep.ai/app/grounddocs-grounddocs)

# GroundDocs

GroundDocs is a version-aware documentation assistant. It connects LLMs to trusted, real-time docs—reducing hallucinations and ensuring accurate, version-specific responses.

## 🚀 Installation

```bash
npx @grounddocs/cli@latest install <client>
```

**Supported clients:** cursor, windsurf, cline, claude, witsy, enconvo, vscode

## 🔧 Manual Setup

To manually configure GroundDocs, add it to your IDE's MCP (Model Context Protocol) configuration:

```json
{
  "mcpServers": {
    "@grounddocs/grounddocs": {
      "command": "npx",
      "args": ["-y", "@grounddocs/grounddocs@latest"]
    }
  }
}
```
After configuration, restart your IDE for the changes to take effect.


📚 Supported Domain

- **Kubernetes** (all versions, including version-aware kubectl behavior, API schemas, and feature gates)

## 🏗️ Architecture

GroundDocs consists of:
- **Local MCP server** (this repo) → lightweight, public, runs inference-time queries
- **Remote backend data repository** (private) → handles scraping, indexing, and heavy lifting

## 🌟 Example Query

```
What changes were made to the kubectl command behavior in Kubernetes 1.26 regarding pruning during apply operations?
```
[View example response](https://claude.ai/share/b864ee23-4899-4092-bbd8-a020d55296a7)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
