# Project 3 — Synthea EHR: Relational Schema Design

**Category:** Data Modeling · **Built:** Week 3, Days 14–19 (~6 hours)

## Question

Given a set of flat, denormalized synthetic EHR exports, what's a well-normalized relational schema for storing patients, encounters, conditions, medications, and observations — and how do you get the data into it safely?

## Dataset

[Synthea](https://synthetichealth.github.io/synthea/) synthetic patient generator — generate (or download a pre-built sample of) a small population (100–500 patients) via the [Synthea GitHub repo](https://github.com/synthetichealth/synthea). Synthea outputs realistic-but-fake CSV exports (`patients.csv`, `encounters.csv`, `conditions.csv`, `medications.csv`, `observations.csv`, etc.) — entirely synthetic, so there are no privacy concerns using it.

## Approach

1. **Inspect** the raw Synthea CSV exports; write a short data dictionary of each table's columns and how tables relate.
2. **Design** an ER diagram (Patient, Encounter, Condition, Medication, Observation, and their keys/relationships); note any normalization issues in the raw exports.
3. **Implement the schema** as DDL (`CREATE TABLE` with primary/foreign keys and constraints) in SQLite or Postgres.
4. **ETL** — a Python script that loads the CSVs into the normalized schema, mapping Synthea's UUIDs to the new keys and preserving referential integrity.
5. **Validate** — row-count checks, orphaned-foreign-key checks, and a few analytical queries that only make sense once the tables are properly joined (e.g. average medications per condition).

## Tools

Python (pandas for ETL), SQL (DDL, SQLite/Postgres), a diagramming tool (e.g. [dbdiagram.io](https://dbdiagram.io) or draw.io) for the ER diagram.

## What "done" looks like

- `diagrams/` — the ER diagram (exported image) plus a short explanation of design decisions
- `sql/schema.sql` — the DDL
- `etl/load_data.py` — the load script
- `sql/validate.sql` — integrity checks
- A findings write-up below on normalization tradeoffs made

## Findings

_(Fill in after completing the project: what normalization decisions you made and why, e.g. how you handled multi-valued fields or denormalized codes in the raw export.)_
