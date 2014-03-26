```yaml
---
Entity\Article:
  type: entity
  table: articles
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    title:
      type: string
      length: 64
    createdBy:
      type: string
      gedmo:
        blameable:
          on: create
    updatedBy:
      type: string
      gedmo:
        blameable:
          on: update
```