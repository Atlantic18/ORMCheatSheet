~~~xml
<entity name="author">
  <field name="firstName"/>
  <field name="lastName"/>
  <field name="birthDate"/>
  <unique-constraints>
    <unique-constraint 
		 name="ix_first_name_last_name_date" 
		 columns="firstName,lastName,birthDate"/>
  </unique-constraints>
</entity>
~~~
