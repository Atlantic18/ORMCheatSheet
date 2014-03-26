~~~yaml
book:
  columns:
    id:
      unique: true
      primary: true
  inheritance:
    extends: itemRecord
    type: column_aggregation
    keyField: item
    keyValue: book
~~~