# PRT563 Assignment 4 - Group Danala 11

This repository contains the Neo4j graph database implementation and query scripts required for the PRT563 Assignment 4 submission, together with supplementary analytics and execution evidence.

## Required submission files

- `import.txt` - complete Task 2 graph database implementation script: constraints, index, node imports, subtype labels and relationship imports.
- `queries.txt` - the four Task 3 Cypher queries.
- `csv/` - all 13 CSV source files required to construct the graph database.

## Reconstructing the graph database

The team used Neo4j Desktop 2.2.1 with Neo4j 2026.09.0 / Cypher 25. For graph analytics, GDS 2026.09.0 was used in the recorded team environment.

1. Create a new empty Neo4j database.
2. Copy all 13 files from `csv/` into the database import directory.
3. Run the statements in `import.txt` in order.
4. Run `validation/validation.txt` before analytics.
5. Run each query in `queries.txt` separately.
6. Run scripts in `analytics/` separately when reproducing the graph analytics tasks.

## Baseline validation

The completed relational-to-graph migration was validated at:

- 140 nodes
- 170 relationships
- 10 `PickupOrder` labels
- 10 `DeliveryOrder` labels
- 0 invalid order subtypes

`PickupOrder` and `DeliveryOrder` are additional labels on `Order` nodes and are not counted as separate nodes.

## Task 3 verified queries

- Query 1 - menu variants between $10 and $20 with a specified crust.
- Query 2 - delivery-order operational view across customer, store, driver, delivery and address.
- Query 3 - stores with average paid order value above the global paid-order average.
- Query 4 - customer order count and total spending.

Execution evidence for all four queries is included under `evidence/`.

## Supplementary material

- `analytics/centrality.txt` - centrality experiments.
- `analytics/similarity.txt` - similarity experiments.
- `analytics/alternative_model_experiment.txt` - alternative graph modelling experiment.
- `validation/validation.txt` - integrity checks for the baseline graph.
- `diagrams/` - graph model diagrams.
- `evidence/` - Neo4j screenshots and recorded execution outputs organised by contributor.
