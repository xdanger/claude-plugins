# Marker Plugin

Convert documents (PDF, EPUB, PPTX, DOCX, XLSX, HTML, images) to Markdown/JSON/HTML using [marker-pdf](https://github.com/datalab-to/marker) with Claude Haiku LLM enhancement.

## Features

- High-quality document to Markdown/JSON/HTML conversion
- Multimodal LLM enhancement for accurate table, math, and form extraction
- Support for multiple document formats: PDF, EPUB, PPTX, DOCX, XLSX, HTML, images
- Multiple output formats: markdown, html, json, chunks (RAG-optimized)
- Multiple LLM backends: Claude, OpenAI, Ollama, Google Gemini
- Preserves formatting, tables, equations, and code blocks

## Prerequisites

```bash
# Install marker-pdf with full document support
uv tool install marker-pdf[full]
```

Requirements:

- Python 3.10+
- PyTorch
- `ANTHROPIC_API_KEY` environment variable (for Claude)

## Skills

### marker

Automatically triggered when user needs to:

- Extract content from PDF, EPUB, PPTX, DOCX, XLSX, images
- Convert documents to Markdown/JSON/HTML format
- Process document files with LLM enhancement
- Extract tables or structured data from documents

## Example Usage

Ask Claude:

- "Convert this PDF to markdown: ./docs/report.pdf"
- "Extract content from ./slides/presentation.pptx"
- "Help me convert this EPUB to markdown"
- "Extract tables from this PDF as JSON"

## Configuration

Default settings:

- Output format: Markdown
- LLM: Claude Haiku 4.5
- LLM service: `marker.services.claude.ClaudeService`
- Image extraction: Disabled (plain text output)

## License

MIT
