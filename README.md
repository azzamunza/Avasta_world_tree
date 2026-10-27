# Avasta World Atlas

A static, browser-based explorer for `world_database.json`.

## Files
- `index.html` — the website UI and client-side data explorer.
- `world_database.json` — the database file loaded by the website.

## Run locally
Modern browsers generally block `fetch()` from `file://` URLs. Serve the folder over HTTP instead.

### Python (Windows / macOS / Linux)
1. Put `index.html` and `world_database.json` in the same folder.
2. Open a terminal in that folder.
3. Run:
   ```bash
   python -m http.server 8000
   ```
4. Open `http://localhost:8000` in your browser.

## Updating the database
Replace `world_database.json` with the newer JSON file, keeping the filename and folder unchanged. Refresh the page or click **Reload JSON**. The page fetches the JSON directly with caching disabled; the data is not embedded in the HTML.

## Included features
- World overview and latest recorded state.
- Recursive record indexing across the database's nested objects and arrays.
- Search across names, IDs, descriptions and JSON content.
- Filters by record type, status, parent branch, and continuity/hallucination flags.
- Record detail view, parent connection path, direct children and expandable hierarchy tree.
- Timeline tab and raw JSON view.
- Export of currently filtered records.

The website is intentionally data-driven. If the JSON schema changes significantly, the generic explorer still displays indexed records, but specialised overview/timeline fields may need adjustment.
