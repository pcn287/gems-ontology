# GEMS ontology

The GEMS ontology describes what the tables of the GEMS database mean. GEMS (GreenFeed Emissions Measurement System) pools enteric methane measurements from GreenFeed systems with the animal, diet, intake and milk records collected in the same studies.

- **Ontology IRI:** `https://w3id.org/gems/ontology`
- **Namespace:** `https://w3id.org/gems/ontology#` (prefix `gems:`)
- **Version:** 0.2.2 (`https://w3id.org/gems/ontology/0.2.2`)
- **File:** [`gems.ttl`](gems.ttl) (OWL in Turtle)
- **Licence:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Creators:** Puchun Niu, Hanlu Zhang, Miel Hostens

## What is in it

| Part | What it is | Example |
|---|---|---|
| Classes (22) | The kinds of record | `gems:Study`, `gems:Animal`, `gems:GreenFeedVisit`, `gems:MilkObservation` |
| Object properties (8) | Links between records | `gems:aboutAnimal`, `gems:belongsToStudy`, `gems:receivesTreatment` |
| Datatype properties (193) | Table columns, with datatype and unit | `gems:col_milk_MilkProduction` |

Where a column matches a term in a public ontology, it carries `skos:exactMatch` or `skos:closeMatch` to that term. Terms come first from the Livestock Health Ontology (LHO), then ATOL, ChEBI, PATO, CMO, FoodOn, ENVO, OBI, TO, LBO and NCIT. Columns with no match are GEMS-only terms. This file refers to those terms by their IRI and does not copy them.

Each column property also records the table and column it comes from (`gems:fromTable`, `gems:fromColumn`), its unit (`gems:unit`) and the kind of match (`gems:matchType`).

## Data

This file holds no animal data. Records in the GEMS knowledge graph use IDs under `https://w3id.org/gems/id/`, for example `https://w3id.org/gems/id/animal/003/2193`.

## Citing

Niu P, Zhang H, Hostens M. GEMS ontology, version 0.2.2. https://w3id.org/gems/ontology
