# Datalab Plugin

Convert documents (PDF, EPUB, PPTX, DOCX, XLSX, HTML, images) to Markdown using the [Datalab](https://www.datalab.to) cloud API.

## Features

- Cloud-based document conversion (no local GPU required)
- Python SDK and REST API support
- Async batch processing for multiple files
- Same conversion quality as marker (powered by marker backend)
- Supports: PDF, EPUB, PPTX, DOCX, XLSX, HTML, images

## Prerequisites

```bash
# Install Datalab Python SDK
uv pip install datalab-python-sdk

# Set API key (get from https://www.datalab.to)
export DATALAB_API_KEY="your_api_key_here"
```

## Skills

### datalab

Automatically triggered when user needs to:

- Convert documents using Datalab cloud API
- Process documents without local GPU
- Batch convert multiple files with async processing

## Example Usage

Ask Claude:

- "Use Datalab API to convert this PDF: ./docs/report.pdf"
- "Convert document using Datalab SDK"
- "Batch convert all PDFs in ./documents using Datalab"

## Datalab vs Marker CLI

| Feature      | Datalab API        | Marker CLI          |
| ------------ | ------------------ | ------------------- |
| Processing   | Cloud-based        | Local               |
| GPU Required | No                 | Yes (recommended)   |
| Setup        | API key only       | Python + PyTorch    |
| Speed        | Fast (cloud GPU)   | Depends on hardware |
| Privacy      | Data sent to cloud | Local processing    |
| Cost         | API credits        | Free                |

## License

MIT
