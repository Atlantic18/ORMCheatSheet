~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="createdAt" type="Timestamp"/>
	<column name="updatedAt" type="Timestamp"/>
	<behavior name="timestampable">
		<parameter name="create_column" value="createdAt"/>
		<parameter name="update_column" value="updatedAt"/>
		<parameter name="disable_updated_at" value="false"/>
	</behavior>
</table>
~~~