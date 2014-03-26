~~~xml
<entity name="author">
  <field name="firstName"/>
  <field name="lastName"/>
  <field name="birthDate"/>
  <indexes>
    <index name="ix_name_last" columns="lastName"/>
  </indexes>
</entity>
~~~
