~~~xml
<entity name="itemRecord" inheritance-type="SINGLE_TABLE">
  <id name="id"/>
  <discriminator-column name="item" type="string"/>
	<discriminator-map>
		<discriminator-mapping class="itemRecord" value="itemRecord"/>
		<discriminator-mapping class="book" value="book"/>
		<discriminator-mapping class="magazine" value="magazine"/>
		<discriminator-mapping class="audioRecord" value="audioRecord"/>
	</discriminator-map>
</entity>
~~~
