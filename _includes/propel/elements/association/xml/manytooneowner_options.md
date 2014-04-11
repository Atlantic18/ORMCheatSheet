~~~xml
<table name="publisher">
  <column name="id" type="integer" size="255" required="true" autoIncrement="true" primaryKey="true"/>
  <unique name="IX_UQ_publisher_id">
    <unique-column name="id"/>
  </unique>
</table>
~~~