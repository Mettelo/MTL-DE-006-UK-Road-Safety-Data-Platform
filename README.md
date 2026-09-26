# MTL-DE-006 — UK Road Safety Data Platform

## Project title
**UK Road Safety Data Platform — Collision, Vehicle & Casualty Data Engineering**

## Project type
Data Engineering · Team project · Production-style portfolio project

## Challenge
The Department for Transport publishes detailed record-level road-safety data covering personal-injury road collisions reported to the police in Great Britain, the vehicles involved and the resulting casualties.

The data is valuable, but it is published as separate coded files. A data team needs a repeatable way to ingest, validate, transform and model those datasets into reliable analytics-ready tables that can support road-safety reporting and analysis.

Your team will build that data platform.

## Official data source
Department for Transport — Road safety open data:

https://www.gov.uk/government/statistical-data-sets/road-safety-open-data

Use the **latest 5 years** files for:
- Collisions
- Vehicles
- Casualties

Also use the official data guide supplied on the same GOV.UK page to interpret coded fields.

### Why this data
This is real UK public-sector operational data rather than a training or Kaggle dataset. It contains separate relational datasets, coded fields, changing specifications and enough volume to require genuine engineering decisions.

## Cost requirement
**The complete project must be achievable at £0.**

No paid cloud account, database, API or deployment service is required for successful completion.

Recommended free stack:
- Python
- DuckDB
- SQL
- dbt Core
- Git
- GitHub
- GitHub Actions free allowance for public repositories

Teams may use another free/open-source equivalent, but the final project must remain reproducible without paid infrastructure.

## Core objective
Build a reproducible local data platform that:

1. ingests the three official raw datasets;
2. preserves an immutable raw layer;
3. validates schema and data quality;
4. transforms coded records into useful analytical structures;
5. models collisions, vehicles and casualties consistently;
6. produces curated analytics-ready tables;
7. supports repeatable annual/incremental ingestion;
8. documents lineage, assumptions and known limitations;
9. provides evidence that the pipeline works end to end.

## Required engineering layers

```
Official DfT CSV files
        ↓
Raw ingestion
        ↓
Validation / profiling
        ↓
Staging / standardisation
        ↓
Core relational models
        ↓
Curated analytical marts
        ↓
QA + analytical outputs
```

## Expected analytical outputs
The platform should make it straightforward for analysts to answer questions such as:
- How have collision and casualty volumes changed across the latest five years?
- Which road-user and vehicle groups appear most frequently in recorded casualties?
- How does casualty severity vary across road types, conditions or locations?
- Which local authorities or police-force areas account for the largest volumes?
- What patterns are visible by time, day, month and road environment?
- How do collision, vehicle and casualty records relate at event level?

These are validation/use-case questions, not a requirement to build a large BI dashboard.

## Team submission model
Each project team must create **its own GitHub repository** for the project.

Recommended naming:

`MTL-DE-006-<team-name>`

The Mettelo project repository is the challenge specification. Do not submit work by modifying this repository.

Each team must:
1. create its own repository;
2. invite the designated Mettelo reviewer/collaborator;
3. follow the mandatory repository structure in `project/REPOSITORY_STRUCTURE.md`;
4. use issues/branches/commits/pull requests as evidence of collaboration;
5. complete `submission/FINAL_SUBMISSION.md`;
6. complete final QA;
7. tag the final accepted version `v1.0-mettelo-submission`;
8. submit the team repository URL.

## Project documents
- [Project brief](project/PROJECT_BRIEF.md)
- [Data source & handling](data/README.md)
- [Mandatory repository structure](project/REPOSITORY_STRUCTURE.md)
- [Deliverables](project/DELIVERABLES.md)
- [Acceptance criteria](project/ACCEPTANCE_CRITERIA.md)
- [Team roles](project/TEAM_ROLES.md)
- [Contribution rules](CONTRIBUTIONS.md)
- [Final submission template](submission/FINAL_SUBMISSION.md)

## Important data note
These statistics cover personal-injury collisions on public roads that were reported to the police and recorded through the STATS19 system. They are not a record of every road incident.

---
**Mettelo — Built for What’s Next**
