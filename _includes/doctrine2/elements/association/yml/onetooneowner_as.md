~~~yaml
itemRecord:
  type: entity
  fields:
  oneToOne:
    ean:
      targetEntity: ean
      inversedBy: itemRecord
      joinColumns:
        eanId:
          referencedColumnName: id
~~~
