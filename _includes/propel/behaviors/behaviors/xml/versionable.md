~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="version" type="Integer"/>
	<behavior name="versionable">
		<parameter name="version_column" value="version"/>
		<parameter name="log_created_at" value="true"/>
		<parameter name="log_created_by" value="true"/>
	</behavior>
</table>
~~~