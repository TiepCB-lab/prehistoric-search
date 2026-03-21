# Database Design

## Design Approach
The database should use a normalized relational structure with PostgreSQL as the system of record. Reference tables are separated from transactional entities to keep the schema extensible and consistent.

## Core Entities
- `creatures`: main records for prehistoric creatures.
- `taxa`: taxonomy hierarchy or classification references.
- `geological_periods`: time-based grouping for creature existence.
- `habitats`: environment references for filtering and categorization.
- `features`: searchable traits such as diet, size, locomotion, or defense.
- `creature_feature`: pivot table for many-to-many feature assignments.

## Relationship Strategy
- One taxon can classify many creatures.
- One geological period can contain many creatures.
- One habitat can be linked to many creatures.
- One creature can have many features.
- One feature can belong to many creatures.

## Scalability Considerations
- Use foreign keys for relational integrity.
- Add indexes to commonly filtered columns such as taxon, period, habitat, and slug.
- Keep creature-specific descriptors flexible so new creature groups can reuse the same core schema.
- Reserve dedicated search indexes or materialized strategies for future optimization if filtering volume grows.
