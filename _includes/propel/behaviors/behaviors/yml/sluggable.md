~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    url:
      type: Varchar
    _propel_behaviors:
      sluggable:
        slug_column: url
        permanent: true
        slug_pattern: /items/{name}
        replacement: -
        separator: /
        replace_pattern: /[^\w\/]+/u
~~~