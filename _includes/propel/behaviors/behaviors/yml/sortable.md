~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    rank:
      type: Integer
    item_id:
      type: Integer
    _propel_behaviors:

      sortable:
        rank_column: rank
        scope_column: item_id
        use_scope: true
~~~