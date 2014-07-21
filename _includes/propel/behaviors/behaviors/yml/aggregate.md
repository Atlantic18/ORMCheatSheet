~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    _propel_behaviors:
      aggregate_column:
        name: no_of_copies
        expression: COUNT (id)
        foreign_table: physicalCopy
~~~