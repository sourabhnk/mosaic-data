# Mosaic public data archive — v1

This directory is the public Mosaic knowledge-graph dump that backs the
paper Nyalkalkar (2026), §9 commitment.

- `RELEASE.md` — human-readable release notes, scope, table list
- `MANIFEST.md` — machine-readable manifest (row counts, SHA-256, columns)
- `LICENSE` — CC BY 4.0
- `*.csv` — one file per dumped table

## How to load into a local Postgres

```bash
# Spin up the reproducibility package, which provides the schema:
git clone https://github.com/sourabhnk/mosaic-reproducibility
cd mosaic-reproducibility
docker compose up -d postgres

# Load each CSV into the matching table:
for f in /path/to/v1/*.csv; do
  table=$(basename "$f" .csv)
  docker compose exec -T postgres psql -U mosaic_user -d mosaic_db \
    -c "\copy $table FROM STDIN CSV HEADER" < "$f"
done
```

## How to verify a single paper figure from this archive

The relation-extraction precision numbers reported in §5.2 of the paper
are derivable directly from `semantic_relations.csv` plus the 531-row
labelled gold sample (also in this archive as
`relations_gold_sample_labeled.csv`). See the paper's §4.2.1 and §4.2.3
for the methodology.

## Re-running tools against the dump

Once loaded, point the reproducibility package's `run_repro` driver
at the loaded database with `DATABASE_URL`:

```bash
DATABASE_URL="postgresql://mosaic_user:mosaic_dev_password@localhost:5432/mosaic_db" \
  python -m scripts.run_repro --output ./output
```

The five tool outputs in `./output/` will then be computed against the
full production graph rather than the fixture mini-KG.

## Re-distribution

CC BY 4.0 — see `LICENSE`. Cite the paper:

> Nyalkalkar S. Mosaic: a knowledge-graph + MCP-tool layer for
> pre-clinical R&D intelligence. bioRxiv (2026).
