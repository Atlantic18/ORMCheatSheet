~~~xml
<entity name="publisher">
  <id name="id"/>
  <one-to-many 
   field="itemRecord" 
   target-entity="itemRecord" 
   mapped-by="publisher" 
   fetch="EAGER" 
   index-by="id">
    <cascade>
	  <cascade-all/>
	  <cascade-merge/>
	  <cascade-persist/>
	  <cascade-refresh/>
	  <cascade-remove/>
    </cascade>
    <order-by>
	  <order-by-field name="id" direction="ASC"/>
    </order-by>
  </one-to-many>
</entity>
~~~
