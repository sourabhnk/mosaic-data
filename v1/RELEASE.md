# Mosaic public data archive — v1

**Released:** 2026-06-03
**Pinned to:** Mosaic preprint (Nyalkalkar, 2026), §9 commitment
**Licence:** CC BY 4.0 (see LICENSE)

**Total rows exported:** 1,204,070
**Total size:** 122.07 MB across 29 CSV files

## Scope

This archive is the production Mosaic knowledge graph as of
2026-06-03, exported from the live Neon Postgres deployment.
Headline figures and metrics reported in §5 of the paper
reproduce from this archive when loaded into a local
Postgres + Apache AGE instance (see README.md).

## Privacy posture

The `persons`, `paper_authors`, and `patent_inventors` tables
are anonymised: name and affiliation columns are dropped;
ORCID (where present) and `person_id` are retained. PubMed and
EPO carry the original name→id mappings under their
public-domain metadata terms — re-derivation is possible but
explicit. The talent-migration tool's k≥2 destination-floor
safeguard (paper §6) is enforced at the tool layer, not the
data layer, so this dump's anonymisation is a separate
conservative choice.

## Tables exported

| Table | Rows | Size (KB) | SHA-256 (12-char prefix) |
|---|---:|---:|---|
| `targets.csv` | 363 | 52.5 | `aceeba977c2a` |
| `compounds.csv` | 12,756 | 3,495.0 | `e1b4de208ce2` |
| `papers.csv` | 35,430 | 43,483.7 | `29971dcdbe0e` |
| `patents.csv` | 14,305 | 7,816.0 | `796782849849` |
| `semantic_relations.csv` | 13,704 | 8,657.2 | `afc441e2c7ea` |
| `compound_targets.csv` | 16,043 | 673.1 | `e0be13a18127` |
| `target_structure_neighbors.csv` | 6,367 | 293.0 | `59fe645bd66a` |
| `target_coessentiality_ext.csv` | 6,865 | 547.0 | `71f071d6ec1f` |
| `target_interactions_ext.csv` | 15,643 | 1,090.6 | `7f39b75f4bfd` |
| `target_variant_pathogenicity.csv` | 322 | 137.8 | `a859e50627fe` |
| `target_essentiality.csv` | 319 | 27.9 | `ef853290c6fe` |
| `target_indications.csv` | 11,452 | 784.8 | `3aea504147bf` |
| `target_pathways.csv` | 1,853 | 59.1 | `94da476b21e0` |
| `compound_indications.csv` | 12,902 | 760.2 | `033dcada8179` |
| `compound_analogs.csv` | 174,969 | 7,793.8 | `f9da73b08b57` |
| `compound_selectivity.csv` | 5,071 | 192.3 | `61eb30e12866` |
| `paper_mentions_target.csv` | 39,951 | 844.7 | `fc3bbebcbe53` |
| `paper_mentions_compound.csv` | 13,341 | 491.0 | `80d3f68ae573` |
| `patent_mentions_target.csv` | 25,436 | 699.3 | `7eb2fbf1b200` |
| `patent_mentions_compound.csv` | 958 | 41.3 | `a6deb18a13a2` |
| `patent_organizations.csv` | 20,772 | 893.4 | `c8a6a66c3c55` |
| `organizations.csv` | 93,967 | 15,320.7 | `f354c9e6e64b` |
| `indications.csv` | 19,617 | 2,460.8 | `96c04c71e690` |
| `trials.csv` | 18,325 | 14,386.1 | `8464939892dd` |
| `resistance_relations.csv` | 724 | 264.3 | `f6fdc45658a7` |
| `kg_metadata.csv` | 1 | 1.1 | `536eaec0cbf4` |
| `persons.csv` | 250,066 | 4,075.7 | `5cb13a561728` |
| `paper_authors.csv` | 319,138 | 7,433.1 | `f3b9483550f5` |
| `patent_inventors.csv` | 73,410 | 2,220.7 | `214103262b6b` |

## Citation

When using this dataset, please cite:

> Nyalkalkar S. Mosaic: a knowledge-graph + MCP-tool layer for
> pre-clinical R&D intelligence. bioRxiv (2026).

And link to this archive release (DOI assigned via Zenodo).