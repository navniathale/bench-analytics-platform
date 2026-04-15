# Consultant Bench Intelligence Platform

## Overview
A end-to-end data pipeline built on Databricks and Delta Lake 
that gives resource managers visibility into consultant 
utilisation, bench costs, and skills coverage across different practice areas.

## Business Problem
Consulting firms lose significant revenue through extended bench 
time. This platform covers:
- Who is on bench, for how long, and at what cost
- Utilisation rates by consultant, practice area, and month
- Skills gaps relative to project demand

## Architecture
Medallion architecture with three layers:
- **Bronze** — raw data landing zone (delta lake)
- **Silver** — cleaned, validated, and joined tables
- **Gold** — business ready aggregations for reporting

## Tech Stack
- Databricks (PySpark, Delta Lake, jupyter notebooks)
- Python (data generation, ingestion)
- SQL (transformations)
- ThoughtSpot (visualisation)
- GitHub (version control)

## Data Model
Six core tables per layer:
- employees
- projects
- assignments
- timesheets
- skills
- bench_periods

## Project Structure
├── ingestion/          # synthetic data generation
├── notebooks/
│   ├── bronze/         # raw ingestion notebooks
│   ├── silver/         # cleaning and validation
│   └── gold/           # business aggregations
└── docs/               # architecture decisions