~~~yaml
  relations:
    publisher:
      class: publisher
      foreignAlias: itemRecord
      onDelete: SET NULL
      onUpdate: CASCADE
      cascade: [(NULL)]
      type: one
      foreignType: many
      local: publisherId
      foreign: id
~~~