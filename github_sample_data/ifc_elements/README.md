# IFC Building Elements

This folder contains 3 anonymized IFC building elements (IfcDoor) extracted from a power distribution facility BIM model.

## Data Format

Each element includes:
- `entity_id`: Anonymized element identifier
- `ifc_type`: IFC entity type (IfcDoor)
- `name` / `name_cn`: Element name in English and Chinese
- `location`: Spatial location in the building
- `attributes`: IFC standard attributes
- `derived_properties`: Calculated properties (e.g., clear width)
- `property_sets`: IFC property set data
- `compliance_status`: Example compliance check result

## IFC Schema

The elements follow the **IFC4** schema standard.

## Property Derivation

Clear width is calculated as:
```
ClearWidth = OverallWidth - 2 × FrameThickness
```

Standard frame thickness is assumed as 25mm per side.

## Fire Rating Classification (Chinese Standard)

| Chinese | English | Fire Resistance |
|---------|---------|-----------------|
| 甲级 | Class A | ≥ 1.5 hours |
| 乙级 | Class B | ≥ 1.0 hours |
| 丙级 | Class C | ≥ 0.5 hours |

## Compliance Check Example

The `compliance_status` field demonstrates how SHACL rules are validated against IFC element properties:

```json
{
  "rule": "配电室门净宽度不应小于1.2m",
  "required_value": 1200,
  "actual_value": 1150,
  "result": "FAIL",
  "message": "Door clear width (1150mm) is less than required minimum (1200mm)"
}
```
