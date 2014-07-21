~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    version:
      type: Integer
    _propel_behaviors:
      versionable:
        version_column: version
        log_created_at: true
        log_created_by: true
~~~