~~~yaml
  actAs:
    Sluggable:
      alias: slug
      builder: Doctrine_Inflector, urlize
      canUpdate: false
      indexName: sluggable
      length: 255
      name: slug
      type: string
      unique: true
      uniqueIndex: true
~~~