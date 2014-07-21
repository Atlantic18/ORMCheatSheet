~~~yaml
itemRecord:
  columns:
    id:
      unique: true
      primary: true
  relations:
    Authors:
      class: author
      refClass: authorHasitemRecord
      local: item_record_id
      foreign: author_id
~~~
