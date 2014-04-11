~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<behavior name="aggregate_column">
		<parameter name="name" value="no_of_copies"/>
		<parameter name="expression" value="COUNT (id)"/>
		<parameter name="foreign_table" value="physicalCopy"/>
	</behavior>
</table>
<table name="physicalCopy">
  <column name="id" primaryKey="true"/>
</table>
~~~