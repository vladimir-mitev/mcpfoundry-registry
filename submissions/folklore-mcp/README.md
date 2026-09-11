# Folklore hosted MCP submission

Current Official MCP Registry release: **1.5.0**.
Canonical endpoint: https://api.helena.bio/folklore/v1/mcp
Setup: https://folklore.helena.bio/integrations
Source: https://github.com/helena-bioinformatics/folklore-mcp

## Transport correction

The earlier manifest incorrectly described the source adapter command as stdio.
The public `folklore-mcp` entry starts an HTTP ASGI server. It is not a stdio
bridge to the hosted service. Connect an HTTP-capable MCP client directly to
the canonical endpoint; no credentials or local installation are required.

The manifest now states Streamable HTTP. The existing registry pipeline requires
a binary section, but that structural check does not establish that the Foundry
installer supports hosted endpoints. Remote installer support requires maintainer
review before this submission can be treated as an executable integration.
The binary metadata identifies the public source entry only.

## Scientific scope

The six listed scientific tools retrieve public variant evidence, literature
and ClinGen Gene-Disease Validity assertions.
Discover the live catalog for the complete hosted surface. Use only public
GRCh38 germline nuclear SNVs or simple indels for variant tools; use exact
gene symbols/HGNC identifiers or disease names/MONDO identifiers for the new
association tools. Never submit patient, phenotype,
family, segregation or private case data. Preserve ambiguous and unavailable
outcomes. Results support professional review and are not diagnosis or treatment
recommendations. Apache-2.0 covers the public adapter, not the separate platform.

`get_gene_disease_associations` and `search_disease_genes` retain assertion-level
source links, inheritance and pagination. A disease-name search can match
multiple diseases. No result is not evidence of no association. ClinGen GDV
is the initial source; this does not claim comprehensive disease-gene coverage.
The hosted catalog has seven tools including a separate `support_helena` helper;
this manifest lists the six scientific operations. The standalone source feature
is opt-in via `FOLKLORE_GENE_DISEASE_ENABLED=true`. No VCF or raw sequencing
upload, batch variant analysis, or patient interpretation is supported.
