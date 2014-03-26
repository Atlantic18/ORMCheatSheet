~~~xml
<entity name="itemRecord">
  <id name="id"/>
  <many-to-many 
   field="authors" 
   target-entity="author" 
   inversed-by="itemRecords">
    <join-table name="authorHasitemRecord">
      <join-columns>
        <join-column 
		name="item_record_id" 
		referenced-column-name="itemRecord_id" 
		nullable="false"/>
      </join-columns>
      <inverse-join-columns>
        <join-column 
		 name="author_id" 
		 referenced-column-name="id" 
		 nullable="false"/>
      </inverse-join-columns>
    </join-table>
  </many-to-many>
</entity>
~~~
