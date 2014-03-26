~~~yaml
publisher:
  type: entity
  fields:
    id:
      id: true
  oneToMany:
    itemRecord:
      targetEntity: itemRecord
      mappedBy: publisher
      fetch: EAGER
      indexBy: id
      cascade: ["all", "merge", "persist", "refresh", "remove"]
      orderBy:
        id: ASC

~~~
