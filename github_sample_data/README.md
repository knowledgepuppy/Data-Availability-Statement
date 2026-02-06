# Sample Data for HITL BIM Compliance Checking

This repository contains anonymized sample data from the research paper:

**"Human-in-the-Loop Semantic Rule Base Generation and Dynamic Updating for Automated BIM Compliance Checking: A Knowledge Graph Approach"**

## Folder Structure

```
github_sample_data/
├── example_clauses/       # 20 annotated regulatory clauses
├── example_rules/         # 10 SHACL validation rules
├── ifc_elements/          # 3 IFC building elements
└── README.md
```

## Data Description

### 1. Example Clauses (`example_clauses/`)
Contains 20 annotated Chinese regulatory clauses from power distribution facility standards. Each clause includes:
- Original Chinese text
- Semantic entity annotations (Subject, Object, Property, Comparison Operator, Reference Value)
- Pattern type classification
- Difficulty level

### 2. Example Rules (`example_rules/`)
Contains 10 SHACL (Shapes Constraint Language) rules translated from regulatory clauses. Each rule includes:
- Source regulatory text
- Extracted semantic entities
- Generated SHACL shape in Turtle format
- Validation target class

### 3. IFC Elements (`ifc_elements/`)
Contains 3 anonymized IFC building elements (IfcDoor) with:
- Entity ID and type
- Geometric attributes (OverallWidth, OverallHeight)
- Derived properties (ClearWidth, FireRating)

## Semantic Entity Types

| Type | Description (English) | Description (Chinese) |
|------|----------------------|----------------------|
| sobj | Subject Object | 主体对象 |
| obj | Controlled Object | 受控对象 |
| prop | Measurable Property | 可量化属性 |
| cmp | Comparison Operator | 比较运算符 |
| Rprop | Reference Value | 参考值 |
| Robj | Reference Object | 参考对象 |
| ARprop | Additional Requirement | 附加要求 |

## License

This sample data is provided for research and educational purposes only. The original regulatory documents are publicly available from the Ministry of Housing and Urban-Rural Development of China (https://www.mohurd.gov.cn).

## Citation

If you use this data in your research, please cite our paper:

```bibtex
@article{zhang2025hitl,
  title={Human-in-the-Loop Semantic Rule Base Generation and Dynamic Updating for Automated BIM Compliance Checking: A Knowledge Graph Approach},
  author={Zhang, Zhuoqun and Zhao, Chunhui and Li, Danli and Li, Peijie and Chen, Yulong and Han, Daguang},
  journal={Buildings},
  year={2025},
  publisher={MDPI}
}
```
