~~~xml
<entity name="publisher">
  <id name="id"/>
  <one-to-many 
   field="itemRecord" 
   target-entity="itemRecord" 
   mapped-by="publisher">
  </one-to-many>
</entity>
~~~