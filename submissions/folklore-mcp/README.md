# Folklore hosted MCP submission

Current Official MCP Registry release: **2.0.0**.
Canonical endpoint: https://api.helena.bio/folklore/v1/mcp
Setup: https://folklore.helena.bio/integrations/mcp
Source: https://github.com/helena-bioinformatics/folklore-mcp

Connect an HTTP-capable MCP client directly to the hosted Streamable HTTP
endpoint. The public source adapter starts an HTTP ASGI server. The manifest
retains the binary section required by the registry pipeline. Maintainer review
is needed to establish whether the Foundry installer supports hosted endpoints.

The hosted endpoint exposes eleven public tools without an API key. The manifest
lists the ten scientific tools. The separate opt-in support helper appears in
live discovery. A Folklore Bearer API key enables eighteen additional case,
approved-source and report tools at the same endpoint. Consult the setup guide
for authenticated workflows and account limits.

Public classification covers supported GRCh38 nuclear germline SNVs and simple
indels smaller than 50 bp. Use public identifiers for the public workflow and
preserve ambiguity, provenance and limitations. Results require qualified
professional review. Apache-2.0 covers the public adapter and contracts.
