~~~YAML
author:
  type: entity
  fields:
    id:
      id: true
  manyToMany:
    itemRecord:
      targetEntity: itemRecord
      inversedBy: author
      cascade: ["all", "refresh"]
      orderBy:
        id: ASC
      joinTable:
        name: itemRecordHasAuthor
        joinColumns:
          authorId:
            referencedColumnName: id
            nullable: false
            fetch: EAGER
            onDelete: CASCADE
            onUpdate: RESTRICT
        inverseJoinColumns:
          bookId:
            referencedColumnName: itemRecord_id
            nullable: false
~~~
