~~~yaml
authorHasitemRecord:
  columns:
    author_id:
      primary: true
      type: integer(255)
      notnull: true
    item_record_id:
      primary: true
      type: integer(255)
      notnull: true
  relations:
    author:
      class: author
      foreignAlias: itemRecord
      local: author_id
      foreign: id
~~~
