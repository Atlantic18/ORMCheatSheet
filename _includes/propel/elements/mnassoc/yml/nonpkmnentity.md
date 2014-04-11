~~~yaml
  authorHasitemRecord:
    _attributes:
      isCrossRef: true
    author_first_name:
      type: Varchar
      required: true
      primaryKey: true
    item_record_id:
      type: integer
      size: 255
      required: true
      primaryKey: true
      foreignTable: itemRecord
      foreignReference: id
    author_last_name:
      type: Varchar
      required: true
      primaryKey: true
    _foreignKeys:
      :
        foreignTable: author
        references:
          - 
            local: author_first_name
            foreign: firstName
          - 
            local: author_last_name
            foreign: lastName
~~~