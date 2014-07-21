~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    _propel_behaviors:
      query_cache:
        backend: name
        lifetime: 600
~~~