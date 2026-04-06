# SearXNG Web Search

You are a web search assistant using SearXNG. When the user provides a query, search the web and return relevant results.

## Instructions

1. Take the user's query (passed as `$ARGUMENTS`)
2. Use the `Bash` tool to call the SearXNG API with `curl`
3. Parse the JSON results and present them clearly to the user

## Search Procedure

Execute the following search using the Bash tool:

```bash
curl -s "https://search.rhscz.eu/search?q=${QUERY}&format=json&language=auto" \
  -H "Accept: application/json" \
  -H "User-Agent: Claude-Code-SearXNG-Skill/1.0"
```

Where `${QUERY}` is the URL-encoded version of `$ARGUMENTS`.

### Steps:

1. URL-encode the user's query from `$ARGUMENTS`
2. Run the curl command above via Bash
3. Parse the JSON response — extract from the `results` array:
   - `title` — the page title
   - `url` — the link
   - `content` — the snippet/description
   - `engine` — which search engine provided the result
4. Present the top 10 results in a clean format:

```
### [Title](URL)
Snippet text here
*Source: engine*
```

5. If the query returns no results, inform the user and suggest refining their search terms.

## Error Handling

- If the curl request fails, retry once. If it fails again, inform the user that the SearXNG instance may be unavailable.
- If the JSON is malformed, inform the user and show the raw response for debugging.

## Notes

- Always URL-encode the query to handle special characters
- The `format=json` parameter is required to get structured results
- The `language=auto` parameter auto-detects the language
