~~~yaml
  actAs:
    Timestampable:
      created:
        alias: createdAt
        disabled: false
        expression: false
        format: Y-m-d H:i:s
        name: created_at
        type: timestamp
      updated:
        alias: updatedAt
        disabled: false
        expression: false
        name: updated_at
        format: Y-m-d H:i:s
        onInsert: true
        type: timestamp
~~~