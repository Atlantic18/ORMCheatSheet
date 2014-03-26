~~~yaml
itemRecord:
  type: entity
  manyToOne:
    publisher:
      targetEntity: publisher
      inversedBy: itemRecord
      joinColumns:
        publisherId:
          referencedColumnName: publisher_id
~~~
