~~~yaml
  itemRecord:
    id:
      primaryKey: true
    publisher_name:
      type: Varchar
    publisher_vat_code:
      type: Varchar
    _uniques:
      IX_UQ_itemRecord_id: [id]
    _foreignKeys:
      :
        foreignTable: publisher
        references:
          - 
            local: publisher_name
            foreign: name
          - 
            local: publisher_vat_code
            foreign: vatCode
~~~