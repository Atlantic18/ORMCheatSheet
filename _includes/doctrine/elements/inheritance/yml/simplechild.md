~~~yaml
book:
  columns:
    id:
      unique: true
      primary: true
  inheritance:
    extends: itemRecord
    type: simple
    keyField: item
    keyValue: book
~~~