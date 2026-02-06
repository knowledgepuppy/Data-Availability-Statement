# Example SHACL Rules

This folder contains 10 SHACL (Shapes Constraint Language) validation rules translated from regulatory clauses.

## Data Format

Each rule includes:
- `rule_id`: Unique rule identifier
- `pattern_type`: Source clause pattern type
- `source_text`: Original Chinese regulatory text
- `source_text_en`: English translation
- `entities`: Extracted semantic entities
- `expected_shacl`: Generated SHACL shape in Turtle format
- `validation_target`: Target IFC/ontology class

## SHACL Constraint Types Used

| Regulatory Expression | SHACL Predicate |
|----------------------|-----------------|
| 不应小于 (shall not be less than) | `sh:minInclusive` |
| 不得大于 (shall not exceed) | `sh:maxInclusive` |
| 应为/宜为 (shall be / should be) | `sh:equals` |
| 不大于 (not exceed) | `sh:maxInclusive` |
| 不小于 (not less than) | `sh:minInclusive` |

## Ontology Namespace

The rules use the following namespace:
- `pg:` - Power Grid Ontology (`http://powergrid.ontology.org/`)

## Example SHACL Shape

```turtle
@prefix sh: <http://www.w3.org/ns/shacl#> .
@prefix pg: <http://powergrid.ontology.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

pg:DistributionRoomDoorWidthShape
    a sh:NodeShape ;
    sh:targetClass pg:DistributionRoomDoor ;
    sh:property [
        sh:path pg:clearWidth ;
        sh:minInclusive "1.2"^^xsd:decimal ;
        sh:message "配电室门净宽度不应小于1.2m" ;
    ] .
```
