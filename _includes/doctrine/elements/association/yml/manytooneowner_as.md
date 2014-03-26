~~~yaml
itemRecord:
  columns:
    id:
      unique: true
      primary: true
    publisherId:
      type: integer(255)
      notnull: true
  relations:
    publisher:
      class: publisher
      foreignAlias: itemRecord
      local: publisherId
      foreign: id
~~~
