~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
    <behavior name="archivable">
		<parameter name="archive_on_insert" value="false"/>
		<parameter name="archive_on_delete" value="false"/>
		<parameter name="archive_on_update" value="false"/>
		<parameter name="archive_class" value="RecordArchive"/>
		<parameter name="archive_table" value="record_archive"/>
		<parameter name="archived_at_column" value="archive_date"/>
		<parameter name="log_archived_at" value="false"/>
	</behavior>
</table>
<table name="record_archive" phpName="RecordArchive">
  <column name="id" required="true" primaryKey="true" type="INTEGER" />
  <column name="title" type="VARCHAR" required="true" primaryString="true" />
  <column name="archived_at" type="TIMESTAMP" />
</table>
~~~