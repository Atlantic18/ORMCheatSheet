~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<behavior name="auto_add_pk">
		<parameter name="type" value="integer"/>
		<parameter name="name" value="id"/>
		<parameter name="autoIncrement" value="true"/>
	</behavior>
~~~