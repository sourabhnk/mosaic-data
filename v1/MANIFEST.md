# Manifest

Machine-readable index of the files in this archive. Each entry
carries the table name, row count, byte size, SHA-256 hex digest,
the column allowlist actually exported (after privacy filtering),
and a one-line note describing the table.

```json
{
  "version": "v1",
  "generated_at": "2026-06-03T12:29:29.455907+00:00",
  "tables": [
    {
      "table": "targets",
      "present": true,
      "rows": 363,
      "sha256": "aceeba977c2a3b385755d2f1c64abe610fa6ca425b7cbe4eed73994836c2eb94",
      "size_bytes": 53776,
      "columns_exported": [
        "chembl_id",
        "created_at",
        "disease_association_count",
        "disease_associations",
        "druggability_tier",
        "entrez_id",
        "function_description",
        "gene_names",
        "go_terms",
        "homology_human_pct",
        "id",
        "name",
        "protein_family",
        "protein_length",
        "safety_flags",
        "selectivity_group",
        "subcellular_location",
        "symbol",
        "target_class",
        "tissue_expression",
        "uniprot_id",
        "updated_at",
        "validation_level"
      ],
      "note": "Curated oncology targets (363 rows in v1). Provenance from UniProt."
    },
    {
      "table": "compounds",
      "present": true,
      "rows": 12756,
      "sha256": "e1b4de208ce2fc5aac343e425ba12ae557e45a97e73ebfe790258b4edd22539c",
      "size_bytes": 3578833,
      "columns_exported": [
        "adme_flags",
        "chembl_id",
        "compound_type",
        "created_at",
        "first_approval",
        "hba",
        "hbd",
        "id",
        "inchikey",
        "indication_class",
        "logp",
        "max_phase",
        "modality",
        "molecular_weight",
        "molecule_type",
        "name",
        "pchembl_value",
        "pref_name",
        "psa",
        "ro5_violations",
        "selectivity_profile",
        "series_id",
        "smiles",
        "synonyms",
        "trade_names",
        "updated_at",
        "withdrawn_flag"
      ],
      "note": "Compounds. ChEMBL r34 lineage; modality is the heuristic SMILES classification."
    },
    {
      "table": "papers",
      "present": true,
      "rows": 35430,
      "sha256": "29971dcdbe0e9bc427e2b2edcc66e8b10ecb9915b3fd34edf930131a025b9225",
      "size_bytes": 44527277,
      "columns_exported": [
        "abstract",
        "citation_count",
        "created_at",
        "doi",
        "id",
        "journal",
        "mesh_terms",
        "pmid",
        "publication_date",
        "study_type",
        "title",
        "updated_at"
      ],
      "note": "Papers with abstracts (PubMed source). DOI via Crossref."
    },
    {
      "table": "patents",
      "present": true,
      "rows": 14305,
      "sha256": "79678284984952209b0dd9d8da639e9bf4cfa1ffc3f9384f0c09129e3957d295",
      "size_bytes": 8003594,
      "columns_exported": [
        "abstract",
        "claim_count",
        "country_code",
        "cpc_codes",
        "created_at",
        "filing_date",
        "id",
        "patent_family_id",
        "priority_date",
        "publication_date",
        "publication_number",
        "title",
        "updated_at"
      ],
      "note": "Patents. EPO + Google Patents."
    },
    {
      "table": "semantic_relations",
      "present": true,
      "rows": 13704,
      "sha256": "afc441e2c7eaec187570881cfb47f51f13b00a08274c0d7ab55b7f703652df1f",
      "size_bytes": 8864926,
      "columns_exported": [
        "confidence",
        "created_at",
        "evidence_text",
        "extraction_batch_id",
        "id",
        "model_name",
        "object_id",
        "object_type",
        "relation_type",
        "source_doc_id",
        "source_doc_type",
        "subject_id",
        "subject_type"
      ],
      "note": "GLiREL-extracted relations (13.7K rows). Confidence in (0, 1]."
    },
    {
      "table": "compound_targets",
      "present": true,
      "rows": 16043,
      "sha256": "e0be13a181278b1c6f952b07da0b719b80e72c39bf07f9b5dd3f1c8dff66a0cd",
      "size_bytes": 689293,
      "columns_exported": [
        "activity_type",
        "assay_type",
        "compound_id",
        "extraction_confidence",
        "mechanism_type",
        "pchembl_value",
        "source",
        "source_doc_id",
        "source_doc_type",
        "target_id",
        "unit",
        "value"
      ],
      "note": "Compound\u2192target activity edges from ChEMBL."
    },
    {
      "table": "target_structure_neighbors",
      "present": true,
      "rows": 6367,
      "sha256": "59fe645bd66a36ab6fd954b2307f083520d0563bcf02a6909520c32fb5f5433e",
      "size_bytes": 299986,
      "columns_exported": [
        "alntmscore",
        "evalue",
        "lddt",
        "neighbor_id",
        "rmsd",
        "target_id",
        "tm_score"
      ],
      "note": "Foldseek TM-score neighbours, top-K per target (paper \u00a75.4.6)."
    },
    {
      "table": "target_coessentiality_ext",
      "present": true,
      "rows": 6865,
      "sha256": "71f071d6ec1f6eea3bc2d365799952017054ddb0782362eb6c340db08e278615",
      "size_bytes": 560083,
      "columns_exported": [
        "correlation",
        "partner_in_mosaic",
        "partner_symbol",
        "rank",
        "source",
        "target_id",
        "updated_at"
      ],
      "note": "DepMap CRISPR co-essentiality (Mosaic-vs-all-genes)."
    },
    {
      "table": "target_interactions_ext",
      "present": true,
      "rows": 15643,
      "sha256": "7f39b75f4bfd0d512a9a6caa35c903eb94e23e2d66fd8c0475e61e300028f36c",
      "size_bytes": 1116765,
      "columns_exported": [
        "confidence_score",
        "interaction_type",
        "partner_in_mosaic",
        "partner_symbol",
        "source_db",
        "target_id",
        "updated_at"
      ],
      "note": "STRING-DB extended PPI (partners outside the in-corpus target set)."
    },
    {
      "table": "target_variant_pathogenicity",
      "present": true,
      "rows": 322,
      "sha256": "a859e50627fe584d03b636687a9c5656bb56d6a017f7ca7d249513ef69f69e89",
      "size_bytes": 141131,
      "columns_exported": [
        "hotspot_residues",
        "license",
        "mean_score",
        "n_variants",
        "pct_pathogenic",
        "source",
        "target_id",
        "uniprot_id",
        "updated_at"
      ],
      "note": "AlphaMissense per-target variant rollups."
    },
    {
      "table": "target_essentiality",
      "present": true,
      "rows": 319,
      "sha256": "ef853290c6fef0a55afeca3dcf6300b1047e36dcdc07c73c675427a08f13d569",
      "size_bytes": 28562,
      "columns_exported": [
        "dependency_fraction",
        "mean_gene_effect",
        "n_models",
        "source",
        "target_id",
        "updated_at"
      ],
      "note": "DepMap per-target essentiality (mean gene effect, dependency fraction)."
    },
    {
      "table": "target_indications",
      "present": true,
      "rows": 11452,
      "sha256": "3aea504147bfe2691b838f777273212640d9150e1e719e37fdf461540c981c40",
      "size_bytes": 803653,
      "columns_exported": [
        "association_score",
        "evidence_type",
        "indication_id",
        "source_doc_id",
        "target_id"
      ],
      "note": "Target\u2194indication associations from Open Targets."
    },
    {
      "table": "target_pathways",
      "present": true,
      "rows": 1853,
      "sha256": "94da476b21e0450f2407b025ae031dd7bbe6576fbbea72c9a18e53f65dee6f11",
      "size_bytes": 60555,
      "columns_exported": [
        "pathway_id",
        "role",
        "target_id"
      ],
      "note": "Target\u2194pathway membership from Reactome."
    },
    {
      "table": "compound_indications",
      "present": true,
      "rows": 12902,
      "sha256": "033dcada81799e57db5f6bb9f7b0aaf1573f27f799dd4fda23d373ad3b930f74",
      "size_bytes": 778464,
      "columns_exported": [
        "clinical_status",
        "compound_id",
        "indication_id",
        "max_phase",
        "source_doc_id"
      ],
      "note": "Compound\u2192indication edges from ChEMBL."
    },
    {
      "table": "compound_analogs",
      "present": true,
      "rows": 174969,
      "sha256": "f9da73b08b5786a4dbb35eda2a03f576c5d5012192ef57a73befc22f3e4510b5",
      "size_bytes": 7980848,
      "columns_exported": [
        "compound_a_id",
        "compound_b_id",
        "shared_scaffold",
        "tanimoto_similarity"
      ],
      "note": "Top-K Tanimoto analog edges."
    },
    {
      "table": "compound_selectivity",
      "present": true,
      "rows": 5071,
      "sha256": "61eb30e1286625657526e3cf86d3370e7edc7588615d5502289bd24943b30146",
      "size_bytes": 196888,
      "columns_exported": [
        "compound_id",
        "measurement_type",
        "primary_target",
        "selectivity_ratio",
        "source_doc_id",
        "target_id"
      ],
      "note": "Compound selectivity profiles (computed)."
    },
    {
      "table": "paper_mentions_target",
      "present": true,
      "rows": 39951,
      "sha256": "fc3bbebcbe53e42075adda10acef231311dcb3b04738344179369d173341b772",
      "size_bytes": 865002,
      "columns_exported": [
        "confidence",
        "context_type",
        "mention_count",
        "paper_id",
        "target_id"
      ],
      "note": "Paper\u2192target mention edges."
    },
    {
      "table": "paper_mentions_compound",
      "present": true,
      "rows": 13341,
      "sha256": "80d3f68ae57315e86adb8a29ecb48d180e1895700fce080c68ad63aa47f53a26",
      "size_bytes": 502763,
      "columns_exported": [
        "compound_id",
        "confidence",
        "context_type",
        "mention_count",
        "paper_id"
      ],
      "note": "Paper\u2192compound mention edges."
    },
    {
      "table": "patent_mentions_target",
      "present": true,
      "rows": 25436,
      "sha256": "7eb2fbf1b200ae18b993e4a96c6659b7d978a58027f9f00e083ff1d7bb23f398",
      "size_bytes": 716068,
      "columns_exported": [
        "confidence",
        "context_type",
        "mention_count",
        "patent_id",
        "target_id"
      ],
      "note": "Patent\u2192target mention edges."
    },
    {
      "table": "patent_mentions_compound",
      "present": true,
      "rows": 958,
      "sha256": "a6deb18a13a20d3054d92467ce2b1ee76422f7a75e7f0c022b7d6d40bea8f2a9",
      "size_bytes": 42303,
      "columns_exported": [
        "compound_id",
        "confidence",
        "context_type",
        "mention_count",
        "patent_id"
      ],
      "note": "Patent\u2192compound mention edges."
    },
    {
      "table": "patent_organizations",
      "present": true,
      "rows": 20772,
      "sha256": "c8a6a66c3c55c30fe752bb356d4e0b0242adf72aae5b98a69e663402d0fa160b",
      "size_bytes": 914829,
      "columns_exported": [
        "org_id",
        "patent_id"
      ],
      "note": "Patent\u2192organization (assignee/applicant) edges."
    },
    {
      "table": "organizations",
      "present": true,
      "rows": 93967,
      "sha256": "f354c9e6e64bb28bc1302d89aab8c1eb146bfeae9ecefd9c74d44d60fc815107",
      "size_bytes": 15688346,
      "columns_exported": [
        "country",
        "created_at",
        "founded_year",
        "id",
        "is_big_pharma",
        "name",
        "org_type",
        "parent_org",
        "therapeutic_focus",
        "updated_at"
      ],
      "note": "Organizations (companies, institutions). Public-domain metadata."
    },
    {
      "table": "indications",
      "present": true,
      "rows": 19617,
      "sha256": "96c04c71e69035d4699780b73aa6148f9e23737adfeabddfe0dfe856f0f0ff98",
      "size_bytes": 2519822,
      "columns_exported": [
        "category",
        "created_at",
        "description",
        "external_id",
        "icd_code",
        "id",
        "is_oncology_subtype",
        "mesh_id",
        "name",
        "parent_id",
        "prevalence_tier",
        "source",
        "synonyms",
        "therapeutic_area"
      ],
      "note": "Indications + sub-indication taxonomy."
    },
    {
      "table": "trials",
      "present": true,
      "rows": 18325,
      "sha256": "8464939892dd1327b824d1cdc757b613de96ba80198555c18b9cf40393f1501c",
      "size_bytes": 14731322,
      "columns_exported": [
        "brief_title",
        "completion_date",
        "conditions",
        "created_at",
        "enrollment",
        "has_results",
        "interventions",
        "last_update_posted",
        "lead_sponsor",
        "nct_id",
        "official_title",
        "overall_status",
        "phase",
        "primary_outcomes",
        "sponsor_class",
        "start_date",
        "study_type",
        "updated_at",
        "why_stopped"
      ],
      "note": "ClinicalTrials.gov rows used by the clinical-pipeline tools."
    },
    {
      "table": "resistance_relations",
      "present": true,
      "rows": 724,
      "sha256": "f6fdc45658a7786b61b5429bb48324c622c2c468d36dc7fa3a7193d324de058c",
      "size_bytes": 270609,
      "columns_exported": [
        "bypass_target_id",
        "confidence",
        "created_at",
        "evidence_text",
        "id",
        "resistance_kind",
        "resistant_target_id",
        "source_doc_id"
      ],
      "note": "Keyword-mined resistance relations (paper \u00a73.3 \u2014 `evidence_type='keyword'`)."
    },
    {
      "table": "kg_metadata",
      "present": true,
      "rows": 1,
      "sha256": "536eaec0cbf407c6a44144a04388da82c02f29da307721d8e0a1f18d1e386b03",
      "size_bytes": 1102,
      "columns_exported": [
        "compound_count",
        "data_sources",
        "edge_count",
        "id",
        "kg_version",
        "last_refresh_at",
        "paper_count",
        "patent_count",
        "relation_count",
        "subindication_count",
        "target_count",
        "therapy_areas"
      ],
      "note": "Singleton scope-banner row (target_count, edge_count, etc.)."
    },
    {
      "table": "persons",
      "present": true,
      "rows": 250066,
      "sha256": "5cb13a5617282be51056a711ede45ae79e41b23ad6f54954e191f6d451960f1c",
      "size_bytes": 4173546,
      "columns_exported": [
        "id",
        "orcid"
      ],
      "note": "Anonymised: name + affiliation dropped per paper \u00a79 release posture. id and orcid retained so talent-migration outputs are structurally reproducible. PubMed and EPO carry the original name\u2192id mapping under their public-domain metadata terms."
    },
    {
      "table": "paper_authors",
      "present": true,
      "rows": 319138,
      "sha256": "f3b9483550f5989b564ecaffa16d63d13b7f2400daada8ed1f1e51653a85e7e7",
      "size_bytes": 7611508,
      "columns_exported": [
        "paper_id",
        "person_id"
      ],
      "note": "Anonymised: name column dropped (see persons.csv). author_position kept where present so authorship-order queries reproduce."
    },
    {
      "table": "patent_inventors",
      "present": true,
      "rows": 73410,
      "sha256": "214103262b6b82a448395c9f8ca67ef8b084344059aee4e0bc9e54f7ceda640d",
      "size_bytes": 2273952,
      "columns_exported": [
        "patent_id",
        "person_id"
      ],
      "note": "Anonymised: name and city columns dropped (see persons.csv). inventor_position kept where present."
    }
  ]
}
```
