~~~yaml
itemRecord:
  columns:
    id:
      unique: true
      primary: true
      type: integer(255)
    publisher_name:
      type: string
    publisher_vat_code:
      type: string
  relations:
    Publisher:
      class: publisher
      foreignAlias: ItemRecord
      local: publisher_name
      foreign: name
~~~