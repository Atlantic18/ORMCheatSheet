~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="publisher_name" type="Varchar"/>
	<column name="publisher_vat_code" type="Varchar"/>
	<unique name="IX_UQ_itemRecord_id">
		<unique-column name="id"/>
	</unique>
	<foreign-key foreignTable="publisher">
		<reference foreign="name" local="publisher_name"/>
		<reference foreign="vatCode" local="publisher_vat_code"/>
	</foreign-key>
</table>
~~~