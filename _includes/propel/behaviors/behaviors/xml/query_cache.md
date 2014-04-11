~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="name" type="Varchar"/>
	<behavior name="query_cache">
		<parameter name="backend" value="name"/>
		<parameter name="lifetime" value="600"/>
	</behavior>
</table>
~~~