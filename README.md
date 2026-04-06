# SearXNG Search Skill for AI Edge Gallery

A web search skill for [AI Edge Gallery](https://github.com/google-ai-edge/gallery) that uses a SearXNG instance to search the web.

![JS](https://img.shields.io/badge/JS-0a9396) ![API](https://img.shields.io/badge/API-2dc653)

## Installation

### From URL (recommended)

1. Open AI Edge Gallery on your device
2. Go to Agent Skills and tap the "Skills" chip
3. Tap (+) > **Load skill from URL**
4. Enter: `https://romainc-lab.github.io/searxng-search-skill/searxng-search`

### From local file

1. Clone this repository
2. Push the skill folder to your device:

```bash
adb push searxng-search/ /sdcard/Download/
```

3. In Edge Gallery, tap (+) > **Import local skill** and select the folder

## Usage

Simply ask the LLM to search for anything:

- "Search for the latest news about AI"
- "Find recipes for chocolate cake"
- "Cherche des informations sur la Tour Eiffel"

The skill auto-detects the language and returns the top 10 results.

## Configuration

The skill uses the SearXNG instance at `https://search.rhscz.eu/search`. To use a different instance, edit the URL in `searxng-search/scripts/index.html`.

## Skill Structure

```
searxng-search/
├── SKILL.md          # Skill metadata and LLM instructions
└── scripts/
    └── index.html    # JavaScript logic (SearXNG API calls)
```
