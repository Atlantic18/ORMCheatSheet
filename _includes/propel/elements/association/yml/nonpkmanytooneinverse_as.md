~~~yaml
  publisher:
    id:
      primaryKey: true
    name:
      type: Varchar
    vatCode:
      type: Varchar
      required: true
    _uniques:
      IX_UQ_publisher_id: [id]
~~~