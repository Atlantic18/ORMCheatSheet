~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    createdAt:
      type: Timestamp
    updatedAt:
      type: Timestamp
    _propel_behaviors:
      timestampable:
        create_column: createdAt
        update_column: updatedAt
        disable_updated_at: false
~~~