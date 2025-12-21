# Marker Plugin

Convert documents (PDF, EPUB, PPTX, DOCX, XLSX, HTML) to Markdown using [marker-pdf](https://github.com/datalab-to/marker) with Claude Haiku LLM enhancement.

## Features

- High-quality document to Markdown conversion
- Multimodal LLM enhancement for accurate image and table extraction
- Support for multiple document formats: PDF, EPUB, PPTX, DOCX, XLSX, HTML
- Preserves formatting, tables, equations, and code blocks

## Prerequisites

```bash
# Install marker-pdf with full document support
uv tool install marker-pdf[full]
```

Requirements:

- Python 3.10+
- PyTorch
- `ANTHROPIC_API_KEY` environment variable

## Skills

### marker

Automatically triggered when user needs to:

- Extract content from PDF, EPUB, PPTX, DOCX, XLSX files
- Convert documents to Markdown format
- Process document files with LLM enhancement

## Example Usage

Ask Claude:

- "Convert this PDF to markdown: ./docs/report.pdf"
- "Extract content from ./slides/presentation.pptx"
- "Help me convert this EPUB to markdown"

## Configuration

Default settings:

- Output format: Markdown
- LLM: Claude Haiku 4.5
- LLM service: `marker.services.claude.ClaudeService`

## License

MIT
