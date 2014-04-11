~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="name" type="Varchar" primaryString="true"/>
	<column name="url" type="Varchar"/>
	<behavior name="sluggable">
		<parameter name="slug_column" value="url"/>
		<parameter name="permanent" value="true"/>
		<parameter name="slug_pattern" value="/items/{name}"/>
		<parameter name="replacement" value="-"/>
		<parameter name="separator" value="/"/>
		<parameter name="replace_pattern" value="/[^\w\/]+/u"/>
	</behavior>
</table>
~~~