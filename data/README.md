# Data Sources

## Official source
Department for Transport — Road safety open data:

https://www.gov.uk/government/statistical-data-sets/road-safety-open-data

The source provides record-level Great Britain road-safety data for collisions, vehicles and casualties.

## Required project scope
Use the **latest 5 years** versions of:

1. Road Safety Data — Collisions — last 5 years
2. Road Safety Data — Vehicles — last 5 years
3. Road Safety Data — Casualties — last 5 years

At project creation time, the latest final validated year is **2025**, so the five-year scope covers **2021–2025**.

## Required reference documentation
Use the official **Open dataset data guide** published on the same GOV.UK page.

The source files contain coded fields. Do not guess category meanings.

## Source facts teams must preserve
The data:
- relates to personal-injury collisions on public roads;
- covers collisions reported to the police and recorded using STATS19;
- includes non-sensitive fields made available publicly;
- can include specification or coding changes over time.

## Data handling rule
Do not commit the full raw CSV files to the team repository.

The team must instead provide one of:
- a reproducible download script; or
- clear documented download instructions plus automated local loading.

Store locally using:

```
data/raw/
data/reference/
data/metadata/
```

## Metadata to record
For each raw file record:
- source organisation;
- source URL;
- dataset/entity;
- period;
- downloaded_at;
- original filename;
- file format;
- row count;
- file size;
- checksum where implemented;
- ingestion status.

## Raw-data principle
Raw source files must remain immutable.

Cleaning and recoding belong in staging/transformation layers.
