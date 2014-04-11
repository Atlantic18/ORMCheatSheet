~~~yaml
  itemRecord:
    name:
      description: regular field
      type: Varchar
      size: 255
      default: Frank
      required: true
      valueSet: Frank, Carl, Victor, Bob
      defaultExpr: /defaultSQLexpression/
      defaultValue: name
      inheritance: single
      inputValidator: /inputValidator/
      lazyLoad: true
      phpName: Name
      phpNamingMethod: underscore
      phpType: Varchar
      primaryVarchar: true
      scale: 0
      tableMapName: /table map name/
      sqlType: /SQL type used in CREATE and ALTER statements/
      peerName: /peer name/
      onDelete: CASCADE
      isCulture: true
~~~
