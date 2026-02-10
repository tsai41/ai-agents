# AI Agents Repository

This repository is the source of truth for shared AI agent definitions and
prompts. Organize agents by domain, then point your tools to this repo so all
agents load the same set.

## Usage

Symlink your tool's local agents directory to this repo so every client shares
one canonical set of agents.

Example (Claude):

```bash
rm -rf ~/.claude/agents
ln -s /path/to/ai-agents ~/.claude/agents
```

Repeat for other tools by replacing the target directory.

## Layout

Each top-level folder groups agents by domain:

- `01-core-development`
- `02-language-specialists`
- `03-infrastructure`
- `04-quality-security`
- `05-data-ai`
- `06-developer-experience`
- `07-specialized-domains`
- `08-business-product`
- `09-meta-orchestration`
- `10-research-analysis`
