# DataMorph

> Convert a blob of structured data between JSON, YAML, CSV, TSV, XML, and TOML in the browser.

**[Live demo](https://datamorph-mlx.vercel.app)**

Moving data between formats normally means finding a converter that handles your specific pair, or writing a one-off script. DataMorph parses any of six formats into a common in-memory structure and re-serializes it into any other, so all thirty combinations work from one page. Every parser and serializer is hand-written in the page — no libraries — and the conversion runs locally, so config files and data samples never leave your machine.

## Features

- Six formats, convertible in any direction: JSON, YAML, CSV, TSV, XML, TOML
- Automatic format detection on paste, so the input type is usually already right
- Per-format options: delimiter (comma/semicolon/pipe) and header row for CSV/TSV, indent width or minified for JSON, quote-all and flow style for YAML, root element name for XML
- Optional alphabetical key sorting on output
- Type casting on parse, so numeric and boolean values survive a round trip through text formats
- Sample documents for each format, a swap button to reverse the conversion, and copy or download of the result

## Stack

- Vanilla JavaScript — a single `index.html` with no framework or runtime dependencies
- Vite as the dev server and build tool
- All six parsers and serializers are implemented from scratch in-page

## Running locally

```bash
npm install
npm run dev
```

---

Part of a series of 91 small web apps. [Browse them all](https://lorenzoylosada.vercel.app).
