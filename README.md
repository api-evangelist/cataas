# Cataas (cataas)

Cataas (Cat as a Service) is a free, open-source REST API that returns random cat images and GIFs with optional tags, filters, sizing, and text overlays. The service is widely embedded in tutorials, demos, README files, and chat applications as a friction-free image source. The canonical implementation lives at github.com/cataas/cataas and runs at cataas.com.

**URL:** [Visit APIs.json URL](https://cataas.com/)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=opensource-api-evangelist&utm_content=repo)

## Tags:

 - Animals, Cats, Images, Open Source, Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## APIs

### Cataas
Random and tagged cat image retrieval with optional sizing, filtering, and text overlay. Includes a JSON catalog API and admin/upload endpoints for the canonical hosted instance.

**Human URL:** [https://cataas.com/](https://cataas.com/)

#### Tags:

 - Cats, Images

#### Properties

- [Documentation](https://cataas.com/)
- [OpenAPI](openapi/cataas-openapi-original.yml)
- [JSONSchema](json-schema/cat-schema.json)
- [JSONSchema](json-schema/count-response-schema.json)
- [JSONSchema](json-schema/upload-cat-request-schema.json)
- [JSONSchema](json-schema/edit-cat-request-schema.json)
- [JSONStructure](json-structure/cat-structure.json)
- [JSONStructure](json-structure/count-response-structure.json)
- [JSONStructure](json-structure/upload-cat-request-structure.json)
- [JSONStructure](json-structure/edit-cat-request-structure.json)
- [Example](examples/cat-example.json)
- [Example](examples/count-response-example.json)
- [Example](examples/upload-cat-request-example.json)
- [Example](examples/edit-cat-request-example.json)
- [NaftikoCapability](capabilities/cataas-cats.yaml)
- [NaftikoCapability](capabilities/cataas-catalog.yaml)
- [NaftikoCapability](capabilities/cataas-upload.yaml)
- [NaftikoCapability](capabilities/cataas-admin.yaml)
- [JavaScript / TypeScript Wrapper (community)](https://github.com/iArmanKarimi/Cataas-API-js)
- [Go Wrapper (community)](https://github.com/iArmanKarimi/Cataas-API-go)
- [PHP Wrapper (community)](https://github.com/chimpook/cataas-api-php)

## Common Properties

- [Website](https://cataas.com/)
- [GitHubOrganization](https://github.com/cataas)
- [Canonical Cataas server (Node.js)](https://github.com/cataas/cataas)
- [Cataas Discord bot](https://github.com/cataas/discord-bot)
- [Cataas Slack slash command](https://github.com/cataas/slack-command)
- [Cataas image editor library](https://github.com/cataas/image-editor)
- [MCP Server (community via Pipeworx Gateway)](https://github.com/pipeworx-io/mcp-cataas)
- [PublicAPIsListing](https://github.com/public-apis/public-apis)
- [SpectralRules](rules/cataas-spectral-rules.yml)
- [Vocabulary](vocabulary/cataas-vocabulary.yaml)
- [JSON-LD](json-ld/cataas-context.jsonld)

## Features

| Name | Description |
|------|-------------|
| Random Cat Image | GET /cat returns a random cat image (JPEG, PNG, or GIF). |
| Tagged Cat Retrieval | GET /cat/{tag} returns a random cat matching one or more comma-separated tags. |
| Animated GIFs | GET /cat/gif returns a random animated cat. |
| Text Overlay | GET /cat/says/{text} renders user-supplied text on top of a random cat with configurable font size, color, and background. |
| Image Filters | filter=blur \| mono \| negate \| custom with per-channel and per-property tuning (brightness, hue, saturation, RGB). |
| Sizing and Cropping | type, width, height, fit, and position query parameters resize and crop the returned image. |
| JSON Catalog API | /api/cats, /api/tags, /api/count expose the catalog programmatically. |
| Content Negotiation | json=true returns a metadata document instead of binary; html=true returns an embedding wrapper page. |
| Free and Unauthenticated | All read endpoints are public and require no API key. |

## Use Cases

| Name | Description |
|------|-------------|
| Tutorials and Demos | Embed live cat images in API tutorials, learn-to-code lessons, and conference demos. |
| README Decoration | Decorate open-source READMEs and personal sites with rotating cat imagery. |
| Chat Bots and Slash Commands | Slack, Discord, and Teams bots fetch random cats on demand via /cat or /cat/says. |
| Mocking Image-Heavy APIs | Stand in for a real image-CDN-backed API while prototyping front-end layouts. |
| Image Pipeline Testing | Exercise resize, format-conversion, and filtering pipelines with predictable image input. |

## Integrations

| Name | Description |
|------|-------------|
| Slack | Official slack-command repo wires /cat into Slack workspaces. |
| Discord | Official discord-bot repo provides a Cataas Discord integration. |
| Pipeworx MCP Gateway | Community MCP server (pipeworx-io/mcp-cataas) wraps the API for use by Claude and other MCP clients. |
| Public APIs Catalog | Listed in the public-apis/public-apis Animals category. |

## Solutions

| Name | Description |
|------|-------------|
| Self-Hosted Catalog | Run your own Cataas instance from cataas/cataas (Node.js + MongoDB + sharp) to power internal demos or branded image services. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Cataas API](openapi/cataas-openapi-original.yml)

### JSON Schema

- [Cat](json-schema/cat-schema.json)
- [CountResponse](json-schema/count-response-schema.json)
- [UploadCatRequest](json-schema/upload-cat-request-schema.json)
- [EditCatRequest](json-schema/edit-cat-request-schema.json)

### JSON Structure

- [Cat](json-structure/cat-structure.json)
- [CountResponse](json-structure/count-response-structure.json)
- [UploadCatRequest](json-structure/upload-cat-request-structure.json)
- [EditCatRequest](json-structure/edit-cat-request-structure.json)

### JSON-LD

- [Cataas Context](json-ld/cataas-context.jsonld)

### Examples

- [cat-example.json](examples/cat-example.json)
- [count-response-example.json](examples/count-response-example.json)
- [upload-cat-request-example.json](examples/upload-cat-request-example.json)
- [edit-cat-request-example.json](examples/edit-cat-request-example.json)

## Capabilities

Naftiko capabilities — one self-contained file per OpenAPI tag, each exposing both a REST adapter and an MCP adapter routed inline through its own consumes block.

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Cataas — Cats](capabilities/cataas-cats.yaml) | Cataas | 7 | Developer / Hobbyist |
| [Cataas — Catalog](capabilities/cataas-catalog.yaml) | Cataas | 3 | Developer / DataScientist |
| [Cataas — Upload](capabilities/cataas-upload.yaml) | Cataas | 1 | Contributor |
| [Cataas — Admin](capabilities/cataas-admin.yaml) | Cataas | 4 | Moderator |

## Vocabulary

- [Cataas Vocabulary](vocabulary/cataas-vocabulary.yaml) — Unified taxonomy mapping 3 resources, 6 actions, 4 workflows, and 5 personas across operational (OpenAPI) and capability (Naftiko) dimensions.

## Rules

- [Cataas Spectral Rules](rules/cataas-spectral-rules.yml) — 30 rules across 12 categories enforcing Cataas API conventions (kebab-case paths, lowerCamelCase operationIds, snake_case schema properties, Title-Case tags, HTTPS-only servers, bearer auth on admin endpoints, mandatory summaries/descriptions/operationIds, Microcks compatibility).

## Notes

This entry was bulk-registered as part of a public-apis catalog sweep on 2026-05-28 and enriched on 2026-05-30 via the full opensource pipeline (18 steps; plans/rate-limits/finops/CRD discovery skipped — Cataas has no hosted commercial offering and is not a Kubernetes-native API).

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
