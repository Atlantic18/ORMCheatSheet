~~~yaml
author:
  columns:
    id:
      unique: true
      primary: true
      type: integer(255)
      notnull: true
    firstName:
      type: string
      notnull: true
    lastName:
      type: string
      notnull: true
    birthDate:
      type: string
  relations:
    ItemRecords:
~~~
