~~~yaml
---
Entity\Article:
  type: entity
  table: articles
  gedmo:
    soft_deleteable:
      field_name: deletedAt
      time_aware: false
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    title:
      type: string
    deletedAt:
      type: date
      nullable: true
~~~