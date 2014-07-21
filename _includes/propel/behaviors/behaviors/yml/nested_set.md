~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    left:
      type: Integer
    right:
      type: Integer
    level:
      type: Integer
    thread_id:
      type: Integer
    _propel_behaviors:
      nested_set:
        left_column: left
        level_column: level
        right_column: right
        scope_column: thread_id
        use_scope: true
~~~