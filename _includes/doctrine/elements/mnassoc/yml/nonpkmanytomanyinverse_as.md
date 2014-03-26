~~~yaml
author:
  columns:
    id:
      unique: true
      primary: true
    firstName:
      type: string
      notnull: true
    lastName:
      type: string
      notnull: true
  relations:
    ItemRecord:
      class: itemRecord
      refClass: author2itemRecord
      local: author_first_name
      foreign: item_record_id
~~~