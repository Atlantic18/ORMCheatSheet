~~~xml
<entity name="author">
  <id name="id"/>
  <many-to-many 
   field="itemRecords" 
   target-entity="itemRecord" 
   mapped-by="authors">
  </many-to-many>
</entity>
~~~
