# Acceptance Criteria

A submission is complete only when the following are evidenced.

## Discovery
- Official DfT source and data guide are documented.
- Source grain and relationships are correctly described.
- Dataset period is stated.
- Limitations of police-reported/STATS19 data are acknowledged.

## Reproducibility
- A new user can follow the README to set up the project.
- Paid services are not required.
- Paths and configuration are portable.
- Raw data can be obtained without undocumented manual processing.

## Ingestion
- All three required source entities are handled.
- Raw inputs remain unchanged.
- Ingestion records source/file metadata.
- Rerunning ingestion does not create uncontrolled duplicates.

## Modelling
- Collision, vehicle and casualty models have clearly defined grain.
- Relationships are documented.
- Curated outputs are analysis-ready.
- Coded fields used in outputs are decoded/documented.

## Data quality
- Primary-key/uniqueness checks exist where applicable.
- Referential-integrity checks exist.
- Missing/invalid value handling is explicit.
- Reconciliation checks compare source and modelled volumes.
- Failed checks are visible rather than silently ignored.

## Engineering quality
- Code is modular and readable.
- Hard-coded user-specific paths are avoided.
- Logging/error handling exists.
- Dependencies are reproducible.
- Secrets/credentials are not committed.

## Analytical validation
- The team demonstrates that curated tables can answer meaningful road-safety questions.
- Output figures can be traced back to modelled data.
- No unsupported causal claims are made.

## Documentation
- Architecture is documented.
- Data model is documented.
- Setup/run/test instructions are complete.
- Known limitations are recorded.
- Future-year ingestion is explained.

## Collaboration
- Contributions are transparent.
- Git history shows meaningful team participation.
- Work is reviewed through PRs where practical.

## Submission
- `submission/FINAL_SUBMISSION.md` is complete.
- Repository is accessible to the designated Mettelo reviewer.
- Final QA is complete.
- Final accepted version is tagged `v1.0-mettelo-submission`.
