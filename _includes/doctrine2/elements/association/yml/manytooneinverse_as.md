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
~~~
