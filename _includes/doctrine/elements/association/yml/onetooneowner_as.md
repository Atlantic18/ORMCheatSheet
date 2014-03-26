~~~yaml
itemRecord:
  columns:
    id:
      unique: true
      primary: true
    eanId:
      unique: true
      type: integer
    ean:
      class: ean
      foreignAlias: itemRecord
      local: eanId
      foreign: id
~~~
