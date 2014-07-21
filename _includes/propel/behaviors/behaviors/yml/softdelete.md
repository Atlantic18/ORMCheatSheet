~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    deleted:
      type: Timestamp
    _propel_behaviors:
      soft_delete:
        deleted_column: deleted
~~~