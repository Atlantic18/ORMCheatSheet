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
      defaultJoin: Criteria::INNER_JOIN
      foreignSchema: /foreign schema name/
      onDelete: RESTRICT
      onUpdate: CASCADE
      phpName: /php name/
      refPhpName: /ref php name/
      skipSql: false
    _uniques:
      IX_UQ_itemRecord_id: [id]
~~~