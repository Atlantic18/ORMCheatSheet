```YAML
itemRecord:
  type: entity
  manyToMany:
    authors:
      targetEntity: author
      inversedBy: itemRecords
      joinTable:
        name: authorHasitemRecord
        joinColumns:
          item_record_id:
            referencedColumnName: itemRecord_id
            nullable: false
        inverseJoinColumns:
          author_id:
            referencedColumnName: id
            nullable: false
```
