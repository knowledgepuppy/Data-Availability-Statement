# Example Clauses

This folder contains 20 annotated regulatory clauses from Chinese building standards for power distribution facilities.

## Data Format

Each clause includes:
- `id`: Unique identifier
- `text`: Original Chinese regulatory text
- `text_en`: English translation
- `entities`: Semantic role annotations
- `pattern`: Clause pattern type (Type_1 to Type_6)
- `difficulty`: Annotation difficulty level

## Entity Types

| Type | Name | Description |
|------|------|-------------|
| `sobj` | Subject Object | The main building element being regulated (e.g., 配电室/distribution room) |
| `obj` | Controlled Object | The specific component being constrained (e.g., 门/door) |
| `prop` | Property | The measurable property (e.g., 净宽度/clear width) |
| `cmp` | Comparison | The comparison operator (e.g., 不应小于/shall not be less than) |
| `Rprop` | Reference Value | The required value (e.g., 1.2m) |
| `Robj` | Reference Object | Reference object for comparative constraints |
| `ARprop` | Additional Requirement | Additional requirements or conditions |

## Pattern Types

- **Type_1**: Basic single-property constraint (Subject + Property + Operator + Value)
- **Type_2**: Object-property constraint (Subject + Object + Property + Operator + Value)
- **Type_3**: Comparative constraint with reference object
- **Type_4**: Equipment/material requirement
- **Type_5**: Equality constraint (should be / shall be)
- **Type_6**: Range constraint (between X and Y)
