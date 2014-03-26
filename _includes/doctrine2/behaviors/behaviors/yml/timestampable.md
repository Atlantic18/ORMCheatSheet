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
    created:
      type: date
      gedmo:
        timestampable:
          on: create
    updated:
      type: datetime
      gedmo:
        timestampable:
          on: update
```