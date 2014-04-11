~~~yaml
  itemRecord:
    id:
      primaryKey: true
    publisherId:
      type: integer
      size: 255
      required: true
      foreignTable: publisher
      foreignReference: id
      onDelete: SETNULL
      onUpdate: CASCADE
    _uniques:
      IX_UQ_itemRecord_id: [id]
~~~