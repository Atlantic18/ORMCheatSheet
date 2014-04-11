~~~xml
<table name="authorHasitemRecord" isCrossRef="true">
	<column name="author_first_name" primaryKey="true"/>
	<column name="item_record_id" primaryKey="true"/>
	<column name="author_last_name" primaryKey="true"/>
	<foreign-key foreignTable="itemRecord">
		<reference local="item_record_id" foreign="id"/>
	</foreign-key>
	<foreign-key foreignTable="author">
		<reference local="author_first_name" foreign="firstName"/>
		<reference local="author_last_name" foreign="lastName"/>
	</foreign-key>
</table>
~~~