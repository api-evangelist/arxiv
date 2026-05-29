# arXiv (arxiv)

arXiv is the open-access e-print repository operated by Cornell Tech, hosting more than two million preprints across physics, mathematics, computer science, quantitative biology, quantitative finance, statistics, electrical engineering, and economics. arXiv exposes two principal programmatic interfaces: a REST Query API that returns Atom 1.0 XML and an OAI-PMH v2.0 endpoint for bulk metadata harvesting, plus daily RSS feeds and Amazon S3 / Kaggle distributions for full-text corpora.

**APIs.yml:** [apis.yml](apis.yml)

## Type
- **x-type:** opensource
- **x-tier:** 1 — Cornell-operated open scholarship infrastructure
- **source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Science & Math

## APIs

### arXiv Query API
REST endpoint for searching arXiv and retrieving article metadata. Supports field-prefix queries, AND/OR/ANDNOT operators, phrase grouping, and date-range filters. Responses are Atom 1.0 XML with arXiv and OpenSearch extensions.
- **Base URL:** `https://export.arxiv.org/api/query`
- [Documentation](https://info.arxiv.org/help/api/user-manual.html)
- [API Reference](https://info.arxiv.org/help/api/user-manual.html#_calling_the_api)
- [Getting Started](https://info.arxiv.org/help/api/basics.html)
- [OpenAPI](openapi/arxiv-query-openapi.yml)
- [JSON Schema — Article](json-schema/arxiv-article-schema.json)
- [JSON Structure — Article](json-structure/arxiv-article-structure.json)
- [Example — Query Articles](examples/arxiv-query-articles-example.json)
- [Python SDK — lukasschwab/arxiv.py](https://pypi.org/project/arxiv/)

### arXiv OAI-PMH API
OAI-PMH v2.0 endpoint for bulk-syncing arXiv metadata. Supports Identify, ListSets, ListMetadataFormats, ListRecords, ListIdentifiers, and GetRecord with `oai_dc`, `arXiv`, and `arXivRaw` formats.
- **Base URL:** `https://oaipmh.arxiv.org/oai`
- [Documentation](https://info.arxiv.org/help/oa/index.html)
- [OpenAPI](openapi/arxiv-oaipmh-openapi.yml)
- [Example — List Records](examples/arxiv-oaipmh-listrecords-example.json)

### arXiv RSS Feeds
Daily RSS feeds of new arXiv submissions, organised by archive and subject category.
- **Base URL:** `https://rss.arxiv.org`
- [Documentation](https://info.arxiv.org/help/rss.html)

### arXiv Bulk Data
Full-text and source bulk distribution: an Amazon S3 Requester-Pays bucket containing every arXiv PDF and source archive, plus a periodically refreshed Kaggle dataset of the metadata corpus.
- [Documentation](https://info.arxiv.org/help/bulk_data.html)
- [Amazon S3 Bulk Buckets](https://info.arxiv.org/help/bulk_data_s3.html)
- [Kaggle arXiv Dataset](https://www.kaggle.com/datasets/Cornell-University/arxiv)

## Common Resources
- [Website](https://arxiv.org)
- [Developer Portal](https://info.arxiv.org/help/api/index.html)
- [Terms of Service](https://info.arxiv.org/help/api/tou.html)
- [Privacy Policy](https://info.arxiv.org/help/policies/privacy_policy.html)
- [Status Page](https://status.arxiv.org/)
- [Blog](https://blog.arxiv.org/)
- [Support](https://info.arxiv.org/help/contact.html)
- [GitHub Organization — arXiv](https://github.com/arXiv)
- [Change Log](https://github.com/arXiv/arxiv-docs/commits/develop)
- [Plans / Pricing](plans/arxiv-plans-pricing.yml)
- [Rate Limits](rate-limits/arxiv-rate-limits.yml)
- [Spectral Rules](rules/arxiv-rules.yml)
- [Vocabulary](vocabulary/arxiv-vocabulary.yml)
- [JSON-LD Context](json-ld/arxiv-context.jsonld)

## Naftiko Capabilities
- [Query Capability](capabilities/shared/arxiv-query.yaml)
- [OAI-PMH Capability](capabilities/shared/arxiv-oaipmh.yaml)
- [Research Discovery Workflow](capabilities/research-discovery.yaml)

## MCP Servers (community)
- [blazickjp/arxiv-mcp-server](https://github.com/blazickjp/arxiv-mcp-server)
- [shoumikdc/arXiv-mcp](https://github.com/shoumikdc/arXiv-mcp)
- [Tejas242/arxiv-mcp](https://github.com/Tejas242/arxiv-mcp)
- [glaforge/arxiv-mcp-server](https://github.com/glaforge/arxiv-mcp-server) (Java/Quarkus)
- [kelvingao/arxiv-mcp](https://github.com/kelvingao/arxiv-mcp)

## SDKs
- [arxiv (Python) — lukasschwab/arxiv.py](https://pypi.org/project/arxiv/)
- [arxivpy (Python) — titipata/arxivpy](https://github.com/titipata/arxivpy)

## Key Source Repos in the arXiv GitHub Org
- [arxiv-search](https://github.com/arXiv/arxiv-search) — Search UI and APIs
- [oaipmh](https://github.com/arXiv/oaipmh) — OAI-PMH service
- [arxiv-feed](https://github.com/arXiv/arxiv-feed) — Atom / RSS feeds
- [arxiv-canonical](https://github.com/arXiv/arxiv-canonical) — JSON schema for arXiv metadata
- [arxiv-browse](https://github.com/arXiv/arxiv-browse) — Article abstract and listing pages
- [arxiv-base](https://github.com/arXiv/arxiv-base) — Supporting libraries

## Tags
Science And Math, Scholarly Publishing, Preprints, Open Access, Research, Open Source, Public APIs

## Rate Limits
arXiv enforces a single shared cadence across the legacy Query, OAI-PMH, and RSS APIs:
- **1 request per 3 seconds**, single connection at a time
- **Max 2,000 results per request**
- **Max 30,000 results per query**

Bulk metadata harvest should go through OAI-PMH with resumption tokens; full-text corpora should use the S3 buckets, not repeated PDF downloads.

## Notes
This entry was bulk-registered on 2026-05-28 from the public-apis catalog and enriched on 2026-05-29 with full API documentation, OpenAPI specs for the Query and OAI-PMH endpoints, JSON Schema / JSON Structure / JSON-LD for the Article entity, Naftiko capabilities, Spectral rules, vocabulary, plans, and rate-limits artifacts, plus a discovery sweep of community MCP servers and Python client libraries.

## Timestamps
- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## Maintainers
- **Kin Lane** — kin@apievangelist.com
