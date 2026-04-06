# SearXNG Search Skill for Claude Code

A Claude Code skill that provides web search capabilities using a SearXNG instance.

## Installation

1. Clone this repository
2. Copy the skill file to your Claude Code agents directory:

```bash
mkdir -p ~/.claude/agents
cp searxng-search.md ~/.claude/agents/
```

3. Restart Claude Code

## Usage

In Claude Code, use the skill by asking to search the web:

```
/searxng-search your search query
```

## Configuration

The skill uses the SearXNG instance at `https://search.rhscz.eu/search`. To use a different instance, edit the URL in `searxng-search.md`.
