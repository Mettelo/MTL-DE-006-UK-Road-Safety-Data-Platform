# Mandatory Team Repository Structure

Each team must create a separate repository named:

`MTL-DE-006-<team-name>`

Minimum structure:

```
MTL-DE-006-<team-name>/
│
├── README.md
├── CONTRIBUTIONS.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── raw/
│   │   └── README.md
│   ├── reference/
│   │   └── README.md
│   └── metadata/
│       └── README.md
│
├── docs/
│   ├── 01-discovery/
│   │   └── README.md
│   ├── 02-data-model/
│   │   └── README.md
│   ├── 03-pipeline-and-quality/
│   │   └── README.md
│   ├── 04-analysis-and-output/
│   │   └── README.md
│   └── 05-technical-handover/
│       └── README.md
│
├── src/
│   ├── ingestion/
│   ├── validation/
│   ├── transformation/
│   └── utils/
│
├── sql/
├── models/
├── tests/
├── notebooks/
├── analysis/
├── outputs/
│
└── submission/
    └── FINAL_SUBMISSION.md
```

## Repository rules

### Raw data
Do **not** commit large DfT CSV files to GitHub.

Instead:
- add raw CSV patterns to `.gitignore`;
- provide repeatable download instructions or an ingestion script;
- preserve source metadata;
- include small samples only when legally permitted and genuinely needed.

### Documentation
The repository must explain:
- what the platform does;
- the architecture;
- how the data moves through each layer;
- how to run it;
- how to test it;
- known limitations;
- who contributed what.

### Collaboration evidence
Use:
- GitHub issues for scoped tasks;
- feature branches;
- meaningful commit messages;
- pull requests for review;
- PR comments/reviews where practical.

Avoid one person uploading the entire project at the end.

## Final version
After QA and Mettelo review, create the tag:

`v1.0-mettelo-submission`
