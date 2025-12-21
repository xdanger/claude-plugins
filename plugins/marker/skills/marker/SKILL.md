---
name: marker
description: Convert documents (PDF, EPUB, PPTX, DOCX, XLSX, HTML) to Markdown using marker-pdf with Claude Haiku LLM enhancement for accurate image and table extraction. Use when user needs to extract content from documents, convert PDFs to markdown, or process document files.
---

# Marker Document Converter

Convert PDF, EPUB, PPTX, DOCX, XLSX, and HTML files to clean Markdown format using the marker-pdf tool with multimodal LLM enhancement.

## Prerequisites

```bash
# Install marker-pdf with full document support
uv tool install marker-pdf[full]
```

Requires Python 3.10+ and PyTorch.

## Usage

When the user provides a document file path, run:

```bash
marker_single "<file_path>" \
  --output_format=markdown \
  --output_dir="<output_directory>" \
  --use_llm \
  --llm_service=marker.services.claude.ClaudeService \
  --claude_model_name=claude-haiku-4-5 \
  --claude_api_key=$ANTHROPIC_API_KEY \
  --disable_image_extraction
```

**Note**: `--disable_image_extraction` generates plain text output. Remove this flag if images need to be preserved.

## Parameters

- `<file_path>`: Path to the input document (PDF, EPUB, PPTX, DOCX, XLSX, HTML)
- `--output_format`: Output format, options: `markdown` (default), `html`, `json`, `chunks`
- `--output_dir`: Directory to save output files (defaults to same directory as input)
- `--use_llm`: Enable LLM-based accuracy improvements for tables, formatting, and form extraction
- `--page_range`: Process specific pages (e.g., "0,5-10,20")

## Examples

### Convert PDF to Markdown

```bash
marker_single "./docs/report.pdf" \
  --output_format=markdown \
  --output_dir="./docs/" \
  --use_llm \
  --llm_service=marker.services.claude.ClaudeService \
  --claude_model_name=claude-haiku-4-5 \
  --claude_api_key=$ANTHROPIC_API_KEY \
  --disable_image_extraction
```

### Convert PPTX to HTML

```bash
marker_single "./slides/presentation.pptx" \
  --output_format=html \
  --output_dir="./slides/" \
  --use_llm \
  --llm_service=marker.services.claude.ClaudeService \
  --claude_model_name=claude-haiku-4-5 \
  --claude_api_key=$ANTHROPIC_API_KEY \
  --disable_image_extraction
```

### Convert specific pages

```bash
marker_single "./docs/book.pdf" \
  --output_format=markdown \
  --output_dir="./docs/" \
  --page_range="1-10" \
  --use_llm \
  --llm_service=marker.services.claude.ClaudeService \
  --claude_model_name=claude-haiku-4-5 \
  --claude_api_key=$ANTHROPIC_API_KEY \
  --disable_image_extraction
```

## Advanced Options

- `--force_ocr`: Force OCR on entire document, converts inline math to LaTeX
- `--redo_inline_math`: Highest quality inline math conversion (use with `--use_llm`)
- `--disable_image_extraction`: Skip image extraction
- `--paginate_output`: Add page separators to output
- `--debug`: Enable diagnostic logging

## Output

The tool generates:

- Formatted Markdown with tables, LaTeX equations ($$-fenced), code blocks
- Extracted images saved alongside the output
- Metadata with table of contents and page statistics

## Instructions

1. Confirm the input file path exists
2. Determine output directory (default: same as input file)
3. Check if `$ANTHROPIC_API_KEY` environment variable is set
4. Run the `marker_single` command with appropriate options
5. Report the output file location and any extraction notes
