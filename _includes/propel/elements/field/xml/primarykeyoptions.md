~~~xml
<column 
 name="id" 
 type="integer" 
 size="255" 
 required="true" 
 autoIncrement="true" 
 primaryKey="true" 
 defaultExpr="/defaultSQLexpression/" 
 description="this is primary key" 
 inheritance="single" 
 lazyLoad="true" 
 phpName="Id" 
 phpNamingMethod="underscore" 
 phpType="integer" 
 primaryVarchar="true" 
 scale="2" 
 onDelete="RESTRICT" 
 peerName="/peer name/" 
 isCulture="true" 
 inputValidator="/input validator/" 
 sqlType="integer" 
 tableMapName="/table map name/"
 />

<unique name="IX_UQ_itemRecord_id">
  <unique-column name="id"/>
</unique>
~~~