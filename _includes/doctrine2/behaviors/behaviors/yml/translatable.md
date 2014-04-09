~~~yaml
---
Entity\Article:
  type: entity
  table: articles
  gedmo:
    translation:
      locale: localeField
# using specific personal translation class:
#     entity: Translatable\Fixture\CategoryTranslation
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    title:
      type: string
      length: 64
      gedmo:
        - translatable
    content:
      type: text
      gedmo:
        - translatable
~~~