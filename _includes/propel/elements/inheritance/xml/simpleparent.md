~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
  <column name="name"/>
  <column name="cover"/>
  <column name="issue"/>
	<column name="item" type="Varchar" inheritance="single">
		<inheritance key="itemRecord" class="itemRecord"/>
		<inheritance key="book" class="book" extends="itemRecord"/>
		<inheritance key="magazine" class="magazine" extends="itemRecord"/>
		<inheritance key="audioRecord" class="audioRecord" extends="itemRecord"/>
	</column>
</table>
~~~
