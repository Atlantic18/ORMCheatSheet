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
    code:
      type: string
      length: 16
    slug:
      type: string
      length: 128
      gedmo:
        slug:
          separator: _
          style: camel
          fields:
            - title
            - code
  indexes:
    search_idx:
      columns: slug
~~~