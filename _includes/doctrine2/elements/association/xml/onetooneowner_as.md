~~~xml
<entity name="itemRecord">
	<one-to-one field="ean" target-entity="ean" inversed-by="itemRecord">
		<join-columns>
			<join-column 
			 name="eanId" 
			 referenced-column-name="id" 
			 unique="true"/>
		</join-columns>
	</one-to-one>
</entity>
~~~
