~~~yaml
  authorHasitemRecord:
    _attributes:
      isCrossRef: true
    author_id:
      type: integer
      size: 255
      required: true
      primaryKey: true
      foreignTable: author
      foreignReference: id
    item_record_id:
      type: integer
      size: 255
      required: true
      primaryKey: true
      foreignTable: itemRecord
      foreignReference: id
~~~
