~~~xml
<table name="authorHasitemRecord" isCrossRef="true">
  <column name="author_id" type="integer" size="255" required="true" primaryKey="true"/>
  <column name="item_record_id" type="integer" size="255" required="true" primaryKey="true"/>
  <foreign-key 
   foreignTable="itemRecord" 
   defaultJoin="Criteria::LEFT_JOIN" 
   onDelete="cascade" 
   onUpdate="cascade" 
   phpName="/php name/" 
   refPhpName="/ref php name/" 
   skipSql="false">
    <reference local="item_record_id" foreign="id"/>
  </foreign-key>
  <foreign-key foreignTable="author" onUpdate="cascade" defaultJoin="Criteria::INNER_JOIN">
    <reference local="author_id" foreign="id"/>
  </foreign-key>
</table>
~~~
