~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="left" type="Integer"/>
	<column name="right" type="Integer"/>
	<column name="level" type="Integer"/>
	<column name="thread_id" type="Integer"/>
	<behavior name="nested_set">
		<parameter name="left_column" value="left"/>
		<parameter name="level_column" value="level"/>
		<parameter name="right_column" value="right"/>
		<parameter name="scope_column" value="thread_id"/>
		<parameter name="use_scope" value="true"/>
	</behavior>
</table>
~~~