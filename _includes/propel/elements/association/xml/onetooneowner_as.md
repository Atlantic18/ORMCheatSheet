~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<foreign-key foreignTable="ean">
		<reference foreign="id" local="eanId"/>
	</foreign-key>
</table>
~~~