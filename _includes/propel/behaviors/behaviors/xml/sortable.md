~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="rank" type="Integer"/>
	<column name="item_id" type="Integer"/>
	<behavior name="sortable">
		<parameter name="rank_column" value="rank"/>
		<parameter name="scope_column" value="item_id"/>
		<parameter name="use_scope" value="true"/>
	</behavior>
</table>
~~~