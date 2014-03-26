~~~yaml
ean:
  type: entity
  fields:
    id:
  oneToOne:
    itemRecord:
      targetEntity: itemRecord
      mappedBy: ean
~~~
