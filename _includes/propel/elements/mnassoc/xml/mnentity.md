~~~xml
<table name="authorHasitemRecord" isCrossRef="true">
	<column name="author_id" primaryKey="true"/>
	<column name="item_record_id" primaryKey="true"/>
	<foreign-key foreignTable="itemRecord">
		<reference local="item_record_id" foreign="id"/>
	</foreign-key>
	<foreign-key foreignTable="author">
		<reference local="author_id" foreign="id"/>
	</foreign-key>
</table>
~~~
