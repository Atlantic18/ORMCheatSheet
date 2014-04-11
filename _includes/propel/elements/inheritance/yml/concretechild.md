~~~yaml
  book:
    id:
      type: integer
      required: true
      autoIncrement: true
      primaryKey: true
    cover:
      type: Varchar
    _uniques:
      IX_UQ_book_id: [id]
~~~