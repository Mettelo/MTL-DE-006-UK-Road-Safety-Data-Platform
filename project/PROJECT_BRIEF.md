# Project Brief

## 1. Business context
Road-safety teams need trustworthy, reusable data to understand where collisions occur, who is affected, which vehicles are involved and how patterns change over time.

The Department for Transport publishes rich record-level data, but operational use requires more than downloading CSV files. The source files must be ingested reliably, decoded, validated, related correctly and transformed into stable analytical models.

## 2. Problem statement
Build a production-style data pipeline and analytical data model for the latest five years of official Great Britain road-safety collision, vehicle and casualty data.

The solution must be reproducible on a normal laptop and must not require paid infrastructure.

## 3. Primary users
Assume the platform serves:
- road-safety analysts;
- local-authority transport teams;
- policy and performance teams;
- data analysts building downstream reports;
- data scientists requiring clean feature-ready tables.

## 4. Source entities
The core source entities are:
- **Collisions** — one record per reported collision;
- **Vehicles** — vehicles associated with each collision;
- **Casualties** — casualties associated with each collision.

The collision identifier must be treated as a key relationship across datasets where supported by the source specification.

## 5. Engineering requirements

### Raw layer
- Download or programmatically ingest the official DfT files.
- Preserve raw files unchanged.
- Record source URL, download date, period, file name and checksum/file metadata.
- Do not manually edit raw source data.

### Staging layer
- Standardise column naming and types.
- Handle missing values explicitly.
- Validate expected schemas.
- Decode selected coded fields using the official data guide.
- Document any fields intentionally excluded.

### Core model
Create stable relational models for:
- collisions;
- vehicles;
- casualties.

Demonstrate and test the one-to-many relationships between collision → vehicles and collision → casualties.

### Curated layer
Create analytical marts that support at minimum:
- collision trends;
- casualty severity;
- road-user / vehicle analysis;
- geography;
- time-based analysis;
- road/environment conditions.

### Pipeline behaviour
The pipeline should support reruns without duplicating records.

Design it so a future annual dataset can be added with minimal code changes.

### Data quality
Tests must cover, where applicable:
- primary-key uniqueness;
- required-field completeness;
- accepted values;
- referential integrity;
- duplicate records;
- impossible/invalid dates;
- basic volume reconciliation between raw and modelled layers.

## 6. Minimum engineering standard
A successful project should demonstrate:
- reproducibility;
- modular code;
- configuration rather than hard-coded local paths;
- structured logging;
- clear error messages;
- automated data-quality checks;
- source-to-target lineage;
- documented assumptions;
- version control and team collaboration.

## 7. Out of scope
The core project does **not** require:
- paid cloud infrastructure;
- real-time streaming;
- a production web application;
- machine learning;
- geospatial routing;
- a full BI dashboard.

Teams may add optional extensions only after the core platform passes acceptance criteria.

## 8. Success definition
A new reviewer should be able to clone the repository, follow the setup instructions, ingest the permitted source files, run the pipeline and reproduce the team's curated tables and validation outputs without undocumented manual steps.
