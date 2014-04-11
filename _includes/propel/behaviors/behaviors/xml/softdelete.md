~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="deleted" type="Timestamp"/>
	<behavior name="soft_delete">
		<parameter name="deleted_column" value="deleted"/>
	</behavior>
</table>
~~~