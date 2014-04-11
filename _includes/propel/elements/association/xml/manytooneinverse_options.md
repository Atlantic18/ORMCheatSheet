~~~xml
<table name="itemRecord">
  <column name="id" primaryKey="true"/>
  <column name="publisherId" type="integer" size="255" required="true"/>
  <unique name="IX_UQ_itemRecord_id">
    <unique-column name="id"/>
  </unique>
  <foreign-key 
   foreignTable="publisher" 
   defaultJoin="Criteria::INNER_JOIN" 
   foreignSchema="/foreign schema name/" 
   onDelete="SETNULL" onUpdate="CASCADE" 
   phpName="/php name/" 
   refPhpName="/ref php name/" 
   skipSql="false">
    <reference foreign="id" local="publisherId"/>
  </foreign-key>
</table>
~~~
