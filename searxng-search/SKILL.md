---
name: searxng-search
description: Search the web using SearXNG and return relevant results for any query.
metadata:
  homepage: https://github.com/RomainC-lab/searxng-search-skill
---

# SearXNG Web Search

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:
- **query**: Required. The user's search query. Extract the core search terms from the user's message.
- **lang**: Optional. The 2-letter language code matching the user's language (e.g., "en", "fr", "de", "es"). Defaults to "auto".

**Constraints:**
- Present the results as a clean, numbered list with the title, a brief snippet, and the source URL for each result.
- Limit your response to the top 5-10 most relevant results.
- If no results are found, inform the user and suggest refining their search terms.
- Your response MUST BE written in the SAME language as the user's original prompt.
