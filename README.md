# pi-searxng

SearXNG web search and HTML-to-markdown fetch extension for [Pi](https://github.com/badlogic/pi-mono).

## Features

- **Web Search** — search the web via a SearXNG instance.
- **Content Fetching** — fetch a URL and convert its HTML to markdown via Readability + turndown. JSON and plain-text content are returned as-is.

GitHub-specific operations (repo trees, files, issues, PRs, workflows, releases) are deliberately **out of scope** — use the `gh` CLI via your shell tool instead.

## Installation

```bash
pi install npm:pi-searxng
```

Or try without installing:

```bash
pi -e npm:pi-searxng
```

## Configuration

Create `~/.pi/searxng.json`:

```json
{
  "searxngUrl": "http://localhost:8080",
  "timeoutMs": 30000,
  "maxResults": 10
}
```

Or set the SearXNG URL via env var:

```bash
export SEARXNG_URL=http://localhost:8080
```

## Tools

### `web_search`

Search the web using SearXNG. Supports time filtering, pagination, language, categories, and engine selection.

### `fetch_content`

Fetch a URL and return markdown. Use `headingsOnly: true` to scout long pages.

### `get_search_results`

Retrieve cached search results by `searchId`.

## System Requirements

- Node.js 18+
- SearXNG instance

## License

MIT
