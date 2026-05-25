# Mathpix (mathpix)
Mathpix builds STEM-grade OCR and document-conversion services. Its Convert API converts images, handwriting, and PDFs into Mathpix Markdown (MMD) — a Markdown superset for math, tables, and chemistry — and then transforms MMD into DOCX, LaTeX, HTML, PDF, and PPTX. The same engine powers Snip (desktop snipping tool, mobile, Chrome extension, collaborative MMD editor) and the enterprise Secure Conversion Service (SCS), with on-premises deployment available. Mathpix has processed 5B+ PDF pages and 3B+ images for 3M+ users and is the OCR layer behind customers including Anthropic, Stanford, and Tencent.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/mathpix/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - OCR, STEM, Math, Chemistry, Document Conversion, PDF, LaTeX, Handwriting, AI, Machine Learning

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Mathpix Image OCR API
Submit a single image (URL or base64) to `POST /v3/text` and receive Mathpix Markdown plus optional structured data, HTML, styled LaTeX, and line- or word-level segmentation. Auto-detects printed vs. handwritten and handles math, text, tables, and chemistry diagrams.

**Human URL:** [https://docs.mathpix.com/reference/post-v3-text](https://docs.mathpix.com/reference/post-v3-text)

- [Documentation](https://docs.mathpix.com/reference/post-v3-text)
- [OpenAPI](openapi/mathpix-image-ocr-api-openapi.yml)
- [JSON Schema — Image Result](json-schema/mathpix-image-result-schema.json)
- [JSON-LD](json-ld/mathpix-context.jsonld)
- [Naftiko Capability — Images](capabilities/image-ocr-images.yaml)
- [Example](examples/mathpix-process-image-example.json)

### Mathpix Document OCR API
Asynchronous PDF and document OCR via `POST /v3/pdf`. Submit by URL or multipart upload, poll status, optionally stream via SSE, and download MMD, Markdown, DOCX, LaTeX (`.tex.zip`), HTML, PPTX, or per-line JSON. Supports `page_ranges`, alphabets, chemistry (SMILES), idiomatic equation arrays, and page-info capture.

**Human URL:** [https://docs.mathpix.com/reference/post-v3-pdf](https://docs.mathpix.com/reference/post-v3-pdf)

- [Documentation](https://docs.mathpix.com/reference/post-v3-pdf)
- [OpenAPI](openapi/mathpix-document-ocr-api-openapi.yml)
- [JSON Schema — Document Result](json-schema/mathpix-document-result-schema.json)
- [Naftiko Capability — Documents](capabilities/document-ocr-documents.yaml)
- [Example](examples/mathpix-process-document-example.json)

### Mathpix Convert API
Transform Mathpix Markdown into DOCX, LaTeX archives, HTML, PDF, PPTX, plain Markdown, and zipped multi-file outputs via `POST /v3/converter`. Synchronous submission returns a `conversion_id` to poll per-format completion and download artifacts.

**Human URL:** [https://docs.mathpix.com/reference/post-v3-converter](https://docs.mathpix.com/reference/post-v3-converter)

- [Documentation](https://docs.mathpix.com/reference/post-v3-converter)
- [OpenAPI](openapi/mathpix-convert-api-openapi.yml)
- [Naftiko Capability — Conversions](capabilities/convert-conversions.yaml)
- [Example](examples/mathpix-convert-markdown-example.json)

### Mathpix Batch API
Submit many image URLs (with optional per-image options) via `POST /v3/batch` and retrieve a results map keyed by caller IDs. Supports optional webhook callbacks. Mathpix recommends polling roughly one second per five images.

**Human URL:** [https://docs.mathpix.com/reference/post-v3-batch](https://docs.mathpix.com/reference/post-v3-batch)

- [Documentation](https://docs.mathpix.com/reference/post-v3-batch)
- [OpenAPI](openapi/mathpix-batch-api-openapi.yml)
- [Naftiko Capability — Batches](capabilities/batch-batches.yaml)
- [Example](examples/mathpix-batch-example.json)

### Mathpix Strokes API
Recognize handwritten math, text, and chemistry from raw stroke coordinates (`x` / `y` arrays) via `POST /v3/strokes`. Pairs with the App Tokens API and `strokes_session_id` for client-side digital-ink capture in browsers and tablets. Request body capped at 512 KB.

**Human URL:** [https://docs.mathpix.com/reference/post-v3-strokes](https://docs.mathpix.com/reference/post-v3-strokes)

- [Documentation](https://docs.mathpix.com/reference/post-v3-strokes)
- [OpenAPI](openapi/mathpix-strokes-api-openapi.yml)
- [Naftiko Capability — Strokes](capabilities/strokes-strokes.yaml)
- [Example](examples/mathpix-strokes-example.json)

### Mathpix App Tokens API
Mint short-lived client-side `app_token` credentials (30 seconds to 12 hours; 5 minutes by default) via `POST /v3/app-tokens` so browsers, mobile clients, and digital-ink surfaces can call Mathpix without exposing the long-lived `app_key`. Token issuance is free.

**Human URL:** [https://docs.mathpix.com/reference/post-v3-app-tokens](https://docs.mathpix.com/reference/post-v3-app-tokens)

- [Documentation](https://docs.mathpix.com/reference/post-v3-app-tokens)
- [OpenAPI](openapi/mathpix-app-tokens-api-openapi.yml)
- [Naftiko Capability — App Tokens](capabilities/app-tokens-tokens.yaml)

### Mathpix OCR Usage API
Aggregate OCR consumption by `usage_type`, `request_args_hash`, or `app_id` over hour/day/week/month timespans via `GET /v3/ocr-usage`. Used to track consumption trends and reconcile billing.

**Human URL:** [https://docs.mathpix.com/reference/ocr-usage](https://docs.mathpix.com/reference/ocr-usage)

- [Documentation](https://docs.mathpix.com/reference/ocr-usage)
- [OpenAPI](openapi/mathpix-ocr-usage-api-openapi.yml)
- [Naftiko Capability — Usage](capabilities/ocr-usage-usage.yaml)

## Commerce & Operations

- [Plans (API Commons)](plans/mathpix-plans-pricing.yml) — Snip Free, Snip Pro ($4.99/mo), Convert API (from $0.002/image), SCS (custom).
- [Rate Limits (API Commons)](rate-limits/mathpix-rate-limits.yml) — per-account concurrency, batch polling cadence, 10 MB converter body cap, 512 KB strokes body cap.
- [FinOps / FOCUS](finops/mathpix-finops.yml) — FOCUS 1.3-aligned cost meters with allocation by `app_id` and `usage_type`.

## Tooling, SDKs & Apps

- [Python SDK — mpxpy](https://github.com/Mathpix/mpxpy)
- [iOS Client](https://github.com/Mathpix/ios-client)
- [CLI — mpx-cli](https://github.com/Mathpix/mpx-cli)
- [API Examples](https://github.com/Mathpix/api-examples)
- [mathpix-markdown-it (MMD renderer)](https://github.com/Mathpix/mathpix-markdown-it)
- [VS Code Extension](https://github.com/Mathpix/vscode-mathpix-markdown)
- [PDF Accessibility Toolkit](https://github.com/Mathpix/PDF_Accessibility)
- [Snip — collaborative MMD editor](https://snip.mathpix.com)
- [Snipping Tool (desktop)](https://snip.mathpix.com/download)
- [Mathpix Console](https://console.mathpix.com)

## Conventions

- [Spectral ruleset](rules/mathpix-rules.yml)
- [Vocabulary](vocabulary/mathpix-vocabulary.yml)
- [JSON-LD context](json-ld/mathpix-context.jsonld)

## Authentication

Server-side: send both `app_id` and `app_key` headers. Client-side: mint a short-lived `app_token` via `POST /v3/app-tokens` and use it in place of the long-lived key. Base URL: `https://api.mathpix.com`.

## Contact

- Support: support@mathpix.com
- Sales: https://mathpix.com/contact-sales
- Console: https://console.mathpix.com
