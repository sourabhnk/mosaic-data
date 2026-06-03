# Mosaic public data archive

[![DOI](https://zenodo.org/badge/1258271777.svg)](https://doi.org/10.5281/zenodo.20529684)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository is the public knowledge-graph data archive for the
Mosaic preprint:

> **Mosaic: a knowledge-graph + MCP-tool layer for pre-clinical R&D
> intelligence.** Sourabh Nyalkalkar, 2026. bioRxiv (DOI pending).

It is the artefact the paper's §9 release statement points readers
at. Headline figures and metrics reported in §5 of the paper
reproduce from this archive when loaded into a local Postgres +
Apache AGE instance.

## DOI

- **Concept DOI (always latest version):**
  [10.5281/zenodo.20529684](https://doi.org/10.5281/zenodo.20529684)
- **paper-v1 snapshot DOI:**
  [10.5281/zenodo.20529685](https://doi.org/10.5281/zenodo.20529685)

When citing the dataset that backs the figures and metrics in the
paper, prefer the paper-v1 snapshot DOI so the citation pins to the
exact rows the paper reports. When citing the archive generally
(e.g. in a tool README that should track the latest release), use
the concept DOI.

## Releases

| Version | Released | Pinned to | Tables | Rows | Size |
|---|---|---|---|---:|---:|
| [`v1/`](v1/) | 2026-06-03 | Mosaic preprint (paper-v1 tag) | 29 | 1,204,070 | 122 MB |

Each release directory ships:

- `RELEASE.md` — human-readable release notes, scope, table list
- `MANIFEST.md` — machine-readable manifest (row counts, SHA-256, columns)
- `README.md` — how to load into a local Postgres
- `LICENSE` — CC BY 4.0
- `*.csv` — one file per dumped table

## Companion repository

The reproducibility package — Docker compose orchestration, slim
query layer, and the driver that produced the §5.4 case-study tool
outputs — is published separately at
<https://github.com/sourabhnk/mosaic-reproducibility>.

The full production source code (ingestion pipelines, MCP server,
agent orchestration) is held in a private repository — see §9 of the
paper for the asymmetric-release rationale.

## Live MCP server

The Mosaic MCP server is publicly accessible at
<https://mcp.getmosaic.dev> with Bearer-token authentication.
Documentation at <https://getmosaic.dev/docs>. The free tier is
sufficient for the read-only queries needed to verify any number in
the paper without downloading this archive.

## Privacy posture

Person tables (`persons`, `paper_authors`, `patent_inventors`) are
anonymised: name and affiliation columns are dropped; ORCID (where
present) and `person_id` are retained so the talent-migration tool's
structural outputs are reproducible without exposing the raw
name→person_id mapping. PubMed and EPO carry the original mappings
under their public-domain metadata terms.

## License

CC BY 4.0 — see [`v1/LICENSE`](v1/LICENSE). Third-party data sources
retain their upstream licences (see RELEASE.md for the list).

## Citation

To cite the **dataset** (paper-v1 snapshot):

```bibtex
@dataset{nyalkalkar2026mosaicdata,
  author    = {Nyalkalkar, Sourabh},
  title     = {{Mosaic public knowledge-graph archive (paper-v1)}},
  year      = {2026},
  publisher = {Zenodo},
  version   = {paper-v1},
  doi       = {10.5281/zenodo.20529685},
  url       = {https://doi.org/10.5281/zenodo.20529685}
}
```

To cite the **paper** (preprint DOI pending bioRxiv acceptance):

```bibtex
@article{nyalkalkar2026mosaic,
  author  = {Nyalkalkar, Sourabh},
  title   = {Mosaic: a knowledge-graph + MCP-tool layer for pre-clinical R\&D intelligence},
  journal = {bioRxiv},
  year    = {2026},
  doi     = {pending}
}
```
