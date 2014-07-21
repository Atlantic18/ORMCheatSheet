~~~yaml
propel:
  itemRecord:
    id:
      type: integer
      primaryKey: true
    name:
      type: Varchar
    _propel_behaviors:
      archivable:
        archive_on_insert: false
        archive_on_delete: false
        archive_on_update: false
        archive_class: MyBookArchive
        archive_table: special_book_archive
        archived_at_column: archive_date
        log_archived_at: false
~~~