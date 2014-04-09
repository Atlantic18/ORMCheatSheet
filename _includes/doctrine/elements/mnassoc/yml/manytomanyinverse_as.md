~~~YAML
author:
  columns:
    id:
      unique: true
      primary: true
  relations:
    ItemRecords:
      class: itemRecord
      refClass: authorHasitemRecord
      local: author_id
      foreign: item_record_id
~~~