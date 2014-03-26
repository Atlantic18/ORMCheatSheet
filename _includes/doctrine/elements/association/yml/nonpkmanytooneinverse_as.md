~~~yaml
publisher:
  columns:
    id:
      unique: true
      primary: true
      type: integer(255)
      notnull: true
      autoincrement: true
    name:
      type: string
    vatCode:
      type: string
      notnull: true
~~~