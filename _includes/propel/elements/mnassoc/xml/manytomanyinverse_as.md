~~~xml
<table name="author">
	<column name="id" primaryKey="true"/>
	<unique name="IX_UQ_author_id">
		<unique-column name="id"/>
	</unique>
</table>
~~~