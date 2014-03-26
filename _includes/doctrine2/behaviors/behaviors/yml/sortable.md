```yaml
---
Entity\Item:
  type: entity
  table: items
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    name:
      type: string
      length: 64
    position:
      type: integer
      gedmo:
        - sortablePosition
    category:
      type: string
      length: 128
      gedmo:
        - sortableGroup
```