~~~yaml
itemRecord:
  options:
    charset: utf8
    type: INNODB
    collate: utf8_unicode_ci
  tableName: item_record
  attributes:
    export: none
  columns:
    id:
      unique: true
      primary: true
      type: integer(255)
    publisherId:
      type: integer(255)
    eanId:
      unique: true
      type: integer
    name:
      unique: true
      type: string(255)
    item:
      default: item_new
      type: string(255)
  indexes:
    ix_name_ean:
      fields: [name, eanId]
      type: unique
    ix_name:
      fields: [name]
  relations:
    publisher:
    ean:
    authors:
~~~
