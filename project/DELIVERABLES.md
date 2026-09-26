# Required Deliverables

## D1 — Discovery & source assessment
Document:
- source purpose;
- latest-five-year files used;
- source ownership;
- licensing/access;
- file sizes and formats;
- key entities;
- grain of each source;
- key relationships;
- known source limitations;
- schema/specification changes relevant to the selected period.

Output:
`docs/01-discovery/README.md`

## D2 — Data architecture & model
Provide:
- architecture diagram;
- raw → staging → core → curated design;
- entity relationship diagram;
- key definitions;
- source-to-target mapping;
- grain of each model.

Output:
`docs/02-data-model/`

## D3 — Reproducible ingestion pipeline
Build code that:
- acquires or loads the official source files;
- validates required inputs;
- records metadata;
- loads data to the chosen free local platform;
- can be rerun safely.

Output:
`src/ingestion/`

## D4 — Transformation layer
Build modular SQL/dbt/Python transformations for:
- collisions;
- vehicles;
- casualties;
- decoded/reference fields;
- curated analytical marts.

Output:
`models/`, `sql/` and/or `src/transformation/`

## D5 — Data-quality framework
Implement automated checks covering:
- uniqueness;
- completeness;
- referential integrity;
- accepted values/ranges;
- duplicate detection;
- volume reconciliation.

Output:
`tests/` and `docs/03-pipeline-and-quality/`

## D6 — Analytics-ready outputs
Produce validated tables that support:
- year/month/day trends;
- geography;
- casualty severity;
- road-user analysis;
- vehicle analysis;
- road/environment conditions.

Output:
`analysis/` and `outputs/`

## D7 — Validation analysis
Use the curated data to demonstrate that the platform is fit for analytical use.

Provide a small set of analytical checks/visuals or tables. The objective is to validate the data product, not to turn the project into a dashboard project.

Output:
`docs/04-analysis-and-output/`

## D8 — Technical handover
Document:
- prerequisites;
- installation;
- configuration;
- end-to-end run commands;
- test commands;
- expected outputs;
- troubleshooting;
- known limitations;
- how to add a future year.

Output:
`docs/05-technical-handover/`

## D9 — Team contribution evidence
Complete:
- `CONTRIBUTIONS.md`;
- issue/branch/PR history;
- ownership of major work packages.

## D10 — Final submission
Complete:
`submission/FINAL_SUBMISSION.md`

Submit the repository URL and final tag.
