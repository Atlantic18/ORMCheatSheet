~~~xml
<table name="publisher">
	<column name="id" primaryKey="true"/>
	<column name="name" type="Varchar"/>
	<column name="vatCode" type="Varchar" required="true"/>
	<unique name="IX_UQ_publisher_id">
		<unique-column name="id"/>
	</unique>
</table>
~~~