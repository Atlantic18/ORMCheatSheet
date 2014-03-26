~~~yaml
book:
  columns:
    id:
      unique: true
      primary: true
  inheritance:
    extends: itemRecord
    type: concrete
    keyField: item
    keyValue: book
~~~