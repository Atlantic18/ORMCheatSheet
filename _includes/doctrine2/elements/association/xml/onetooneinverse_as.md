~~~xml
<entity name="ean">
  <id name="id"/>
    <one-to-one 
	 field="itemRecord" 
	 target-entity="itemRecord" 
	 mapped-by="ean">
  </one-to-one>
</entity>
~~~
