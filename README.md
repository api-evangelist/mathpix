# Mathpix (mathpix)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mathpix/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mathpix/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- OCR
- STEM
- Math
- Chemistry
- Document Conversion
- PDF
- LaTeX
- Handwriting
- AI
- Machine Learning

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Mathpix Image OCR API

Submit a single image (by URL or base64) to v3/text and receive Mathpix Markdown plus optional structured data, HTML, styled LaTeX, and line- or word-level segmentation. Auto-detects printed vs. handwritten content and handles math, text, tables, and chemistry diagrams.

- **Human URL:** [https://docs.mathpix.com/reference/post-v3-text](https://docs.mathpix.com/reference/post-v3-text)

#### Tags

- OCR
- STEM
- Math
- Images

#### Properties

- [Documentation](https://docs.mathpix.com/reference/post-v3-text)
- [OpenAPI](openapi/mathpix-image-ocr-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mathpix-image-ocr-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mathpix-image-ocr-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/mathpix-image-result-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/mathpix-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/mathpix-process-image-example.json)

### Mathpix Document OCR API

Asynchronous PDF and document OCR via v3/pdf. Submit by URL or multipart upload, poll status, optionally stream via SSE, and download outputs in MMD, Markdown, DOCX, LaTeX (.tex.zip), HTML, PPTX, or per-line JSON. Supports page ranges, alphabets, chemistry (SMILES), idiomatic equation arrays, and page-info capture.

- **Human URL:** [https://docs.mathpix.com/reference/post-v3-pdf](https://docs.mathpix.com/reference/post-v3-pdf)

#### Tags

- OCR
- PDF
- Documents
- STEM
- Conversion

#### Properties

- [Documentation](https://docs.mathpix.com/reference/post-v3-pdf)
- [OpenAPI](openapi/mathpix-document-ocr-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/mathpix-document-result-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/mathpix-process-document-example.json)

### Mathpix Convert API

Transform Mathpix Markdown into DOCX, LaTeX archives, HTML, PDF, PPTX, plain Markdown, and zipped multi-file outputs. Synchronous submission returns a conversion_id used to poll per-format completion and download artifacts.

- **Human URL:** [https://docs.mathpix.com/reference/post-v3-converter](https://docs.mathpix.com/reference/post-v3-converter)

#### Tags

- Conversion
- Markdown
- DOCX
- LaTeX
- PDF
- PPTX

#### Properties

- [Documentation](https://docs.mathpix.com/reference/post-v3-converter)
- [OpenAPI](openapi/mathpix-convert-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mathpix-convert-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mathpix-convert-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/mathpix-convert-markdown-example.json)

### Mathpix Batch API

Submit many image URLs (with optional per-image options) in a single v3/batch request, poll once per ~5 images, and retrieve a results map keyed by caller-defined identifiers. Supports optional webhook callbacks.

- **Human URL:** [https://docs.mathpix.com/reference/post-v3-batch](https://docs.mathpix.com/reference/post-v3-batch)

#### Tags

- Batch
- OCR
- Images

#### Properties

- [Documentation](https://docs.mathpix.com/reference/post-v3-batch)
- [OpenAPI](openapi/mathpix-batch-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mathpix-batch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mathpix-batch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/mathpix-batch-example.json)

### Mathpix Strokes API

Recognize handwritten math, text, and chemistry from raw stroke coordinates (x/y arrays) via v3/strokes. Pairs with the App Tokens API and strokes_session_id for client-side digital-ink capture in browsers and tablets.

- **Human URL:** [https://docs.mathpix.com/reference/post-v3-strokes](https://docs.mathpix.com/reference/post-v3-strokes)

#### Tags

- Handwriting
- Digital Ink
- OCR
- STEM

#### Properties

- [Documentation](https://docs.mathpix.com/reference/post-v3-strokes)
- [OpenAPI](openapi/mathpix-strokes-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mathpix-strokes-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mathpix-strokes-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/mathpix-strokes-example.json)

### Mathpix App Tokens API

Mint short-lived client-side app_token credentials (30 seconds to 12 hours; 5 minutes by default) so browsers, mobile clients, and digital-ink surfaces can call Mathpix without exposing the long-lived app_key. Token issuance is free.

- **Human URL:** [https://docs.mathpix.com/reference/post-v3-app-tokens](https://docs.mathpix.com/reference/post-v3-app-tokens)

#### Tags

- Authentication
- Tokens
- Security

#### Properties

- [Documentation](https://docs.mathpix.com/reference/post-v3-app-tokens)
- [OpenAPI](openapi/mathpix-app-tokens-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mathpix-app-tokens-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mathpix-app-tokens-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mathpix OCR Usage API

Query OCR consumption metrics aggregated by usage_type, request_args_hash, or app_id, over arbitrary timespans (hour, day, week, month). Used to track consumption trends and reconcile billing.

- **Human URL:** [https://docs.mathpix.com/reference/ocr-usage](https://docs.mathpix.com/reference/ocr-usage)

#### Tags

- Usage
- Metering
- FinOps
- Administration

#### Properties

- [Documentation](https://docs.mathpix.com/reference/ocr-usage)
- [OpenAPI](openapi/mathpix-ocr-usage-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mathpix-ocr-usage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mathpix-ocr-usage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/mathpix)
- [Twitter](https://twitter.com/MathpixApp)
- [Git Hub](https://github.com/Mathpix)
- [Portal](https://docs.mathpix.com)
- [Documentation](https://docs.mathpix.com/reference/introduction)
- [Documentation](https://docs.mathpix.com/guides/authentication)
- [Pricing](https://mathpix.com/pricing)
- [Sign Up](https://accounts.mathpix.com/signup)
- [Login](https://accounts.mathpix.com/login)
- [Console](https://console.mathpix.com)
- [Blog](https://mathpix.com/blog)
- [Support](mailto:support@mathpix.com)
- [Contact Sales](https://mathpix.com/contact-sales)
- [Terms of Service](https://mathpix.com/terms-of-service)
- [Privacy Policy](https://mathpix.com/privacy)
- [SDK](https://github.com/Mathpix/mpxpy)
- [SDK](https://github.com/Mathpix/ios-client)
- [C L I](https://github.com/Mathpix/mpx-cli)
- [Samples](https://github.com/Mathpix/api-examples)
- [Tools](https://github.com/Mathpix/mathpix-markdown-it)
- [Tools](https://github.com/Mathpix/vscode-mathpix-markdown)
- [Tools](https://github.com/Mathpix/PDF_Accessibility)
- [Application](https://snip.mathpix.com)
- [Application](https://snip.mathpix.com/download)
- [Application](https://chromewebstore.google.com/detail/mathpix-snipping-tool/)
- [Plans](plans/mathpix-plans-pricing.yml)
- [Rate Limits](rate-limits/mathpix-rate-limits.yml)
- [Fin Ops](finops/mathpix-finops.yml)
- [Vocabulary](vocabulary/mathpix-vocabulary.yml)
- [Spectral Rules](rules/mathpix-rules.yml)
- [JSON-LD](json-ld/mathpix-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
