~~~yaml
  relations:
    itemRecord:
      class: itemRecord
      foreignAlias: publisher
      onDelete: SET NULL
      onUpdate: CASCADE
      cascade: [(NULL)]
      type: many
      foreignType: one
      local: id
      foreign: publisherId
~~~
