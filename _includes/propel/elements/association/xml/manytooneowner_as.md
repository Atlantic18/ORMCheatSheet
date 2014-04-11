~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<foreign-key foreignTable="publisher">
		<reference foreign="id" local="publisherId"/>
	</foreign-key>
</table>
~~~
