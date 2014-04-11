~~~yaml
  itemRecord:
    id:
      primaryKey: true
    publisherId:
      type: integer
      size: 255
      required: true
      foreignTable: publisher
      foreignReference: id
~~~
