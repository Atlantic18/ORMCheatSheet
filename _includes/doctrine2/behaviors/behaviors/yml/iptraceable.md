~~~yaml
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
    createdFromIp:
      type: string
      length: 45
      nullable: true
      gedmo:
        ipTraceable:
          on: create
    updatedFromIp:
      type: string
      length: 45
      nullable: true
      gedmo:
        ipTraceable:
          on: update
~~~