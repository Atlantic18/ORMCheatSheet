~~~xml
<entity name="author">
  <id name="id" type="integer">
    <generator strategy="AUTO"/>
  </id>
  <field name="firstName" type="string" nullable="false"/>
  <field name="lastName" type="string" nullable="false"/>
  <field name="birthDate" type="string" nullable="true"/>
  <field name="awards" type="string" nullable="true"/>
  <indexes>
    <index name="ix_name_last" columns="lastName"/>
  </indexes>
  <unique-constraints>
    <unique-constraint
     name="ix_first_name_last_name_date" 
     columns="firstName,lastName,birthDate"/>
  </unique-constraints>
  <many-to-many 
   field="itemRecords" 
   target-entity="itemRecord" 
   mapped-by="authors">
    <cascade>
      <cascade-all/>
      <cascade-merge/>
      <cascade-persist/>
      <cascade-refresh/>
      <cascade-remove/>
    </cascade>
    <order-by>
      <order-by-field name="lastName" direction="ASC"/>
    </order-by>
  </many-to-many>
</entity>
~~~
