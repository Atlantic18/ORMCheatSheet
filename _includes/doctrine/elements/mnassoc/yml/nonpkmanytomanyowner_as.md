~~~yaml
itemRecord:
  columns:
    id:
      unique: true
      primary: true
    publisher_name:
      type: string
    publisher_vat_code:
      type: string
    name:
      unique: true
      type: string(255)
    item:
      default: item_new
      type: string(255)
  relations:
    Author:
      class: author
      refClass: author2itemRecord
      local: item_record_id
      foreign: author_first_name
~~~