# arXiv (arxiv)

arXiv is the open-access e-print repository operated by Cornell Tech, hosting more than two million preprints across physics, mathematics, computer science, quantitative biology, quantitative finance, statistics, electrical engineering, and economics. arXiv exposes two principal programmatic interfaces: a REST Query API that returns Atom 1.0 XML and an OAI-PMH v2.0 endpoint for bulk metadata harvesting, plus daily RSS feeds and Amazon S3 / Kaggle distributions for full-text corpora.

**APIs.json:** [https://info.arxiv.org/help/api/index.html](https://info.arxiv.org/help/api/index.html)

## Tags

- Science And Math
- Scholarly Publishing
- Preprints
- Open Access
- Research
- Open Source
- Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### arXiv Query API

REST endpoint for searching arXiv and retrieving article metadata. Supports field-prefix queries (ti, au, abs, co, jr, cat, rn, id, all), AND/OR/ANDNOT operators, phrase grouping, and date-range filters on submittedDate and lastUpdatedDate. Responses are Atom 1.0 XML with arXiv and OpenSearch extensions.

- **Human URL:** [https://info.arxiv.org/help/api/user-manual.html](https://info.arxiv.org/help/api/user-manual.html)
- **Base URL:** `https://export.arxiv.org/api/query`

#### Tags

- Science And Math
- Scholarly Publishing

#### Properties

- [Documentation](https://info.arxiv.org/help/api/user-manual.html)
- [API Reference](https://info.arxiv.org/help/api/user-manual.html#_calling_the_api)
- [Getting Started](https://info.arxiv.org/help/api/basics.html)
- [OpenAPI](openapi/arxiv-query-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arxiv-query.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arxiv-query.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/arxiv-article-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/arxiv-article-structure.json)
- [Example](examples/arxiv-query-articles-example.json)
- [SDK](https://pypi.org/project/arxiv/)

### arXiv OAI-PMH API

Open Archives Initiative Protocol for Metadata Harvesting v2.0 endpoint for bulk-syncing arXiv metadata. Supports Identify, ListSets, ListMetadataFormats, ListRecords, ListIdentifiers, and GetRecord with oai_dc, arXiv, and arXivRaw metadata formats. Metadata refreshes ~10:30pm ET Sunday-Thursday.

- **Human URL:** [https://info.arxiv.org/help/oa/index.html](https://info.arxiv.org/help/oa/index.html)
- **Base URL:** `https://oaipmh.arxiv.org/oai`

#### Tags

- Scholarly Publishing
- Bulk Data

#### Properties

- [Documentation](https://info.arxiv.org/help/oa/index.html)
- [OpenAPI](openapi/arxiv-oaipmh-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arxiv-oaipmh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arxiv-oaipmh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/arxiv-oaipmh-listrecords-example.json)

### arXiv RSS Feeds

Daily RSS feeds of new arXiv submissions, organised by archive and subject category. Primarily intended for human consumption; the OAI-PMH and query APIs are recommended for machine integration.

- **Human URL:** [https://info.arxiv.org/help/rss.html](https://info.arxiv.org/help/rss.html)
- **Base URL:** `https://rss.arxiv.org`

#### Tags

- Scholarly Publishing
- Feeds

#### Properties

- [Documentation](https://info.arxiv.org/help/rss.html)
- [Postman Collection](collections/arxiv-oaipmh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arxiv-oaipmh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/arxiv-query.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arxiv-query.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### arXiv Bulk Data

Full-text and source bulk distribution channels: an Amazon S3 Requester-Pays bucket containing every arXiv PDF and source archive, plus a periodically refreshed Kaggle dataset of the complete metadata corpus.

- **Human URL:** [https://info.arxiv.org/help/bulk_data.html](https://info.arxiv.org/help/bulk_data.html)
- **Base URL:** `https://info.arxiv.org/help/bulk_data_s3.html`

#### Tags

- Bulk Data
- Open Data

#### Properties

- [Documentation](https://info.arxiv.org/help/bulk_data.html)
- [Resources](https://info.arxiv.org/help/bulk_data_s3.html)
- [Resources](https://www.kaggle.com/datasets/Cornell-University/arxiv)
- [Postman Collection](collections/arxiv-oaipmh.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arxiv-oaipmh.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/arxiv-query.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arxiv-query.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://arxiv.org)
- [Developer Portal](https://info.arxiv.org/help/api/index.html)
- [Documentation](https://info.arxiv.org/help/api/user-manual.html)
- [Terms of Service](https://info.arxiv.org/help/api/tou.html)
- [Privacy Policy](https://info.arxiv.org/help/policies/privacy_policy.html)
- [Status Page](https://status.arxiv.org/)
- [Blog](https://blog.arxiv.org/)
- [Support](https://info.arxiv.org/help/contact.html)
- [GitHub Organization](https://github.com/arXiv)
- [Changelog](https://github.com/arXiv/arxiv-docs/commits/develop)
- [Plans](plans/arxiv-plans-pricing.yml)
- [Rate Limits](rate-limits/arxiv-rate-limits.yml)
- [Spectral Rules](rules/arxiv-rules.yml)
- [Vocabulary](vocabulary/arxiv-vocabulary.yml)
- [JSON-LD](json-ld/arxiv-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Public APIs Listing](https://github.com/public-apis/public-apis)
- [Tools](https://github.com/blazickjp/arxiv-mcp-server)
- [Tools](https://github.com/shoumikdc/arXiv-mcp)
- [Tools](https://github.com/Tejas242/arxiv-mcp)
- [Tools](https://github.com/glaforge/arxiv-mcp-server)
- [Tools](https://github.com/kelvingao/arxiv-mcp)
- [SDK](https://pypi.org/project/arxiv/)
- [SDK](https://github.com/titipata/arxivpy)
- [GitHub Repository](https://github.com/arXiv/arxiv-search)
- [GitHub Repository](https://github.com/arXiv/oaipmh)
- [GitHub Repository](https://github.com/arXiv/arxiv-feed)
- [GitHub Repository](https://github.com/arXiv/arxiv-canonical)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
