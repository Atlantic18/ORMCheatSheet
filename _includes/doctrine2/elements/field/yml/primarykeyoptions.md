~~~yaml
itemRecord:
  type: entity
  fields:
    id:
      id: true
      type: integer
      length: 255
      column: itemRecord_id
      columnDefinition: itemRecord_id
      precision: 3
      scale: 3
      version: true
      generator:
        strategy: SEQUENCE
      sequence-generator:
        allocationSize: 1
        initialValue: 1
        sequenceName: itemRecord_id_seq
      options:
        unsigned: true
        comment: this is primary key
        version: 2
~~~
