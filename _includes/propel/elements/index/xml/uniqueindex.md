~~~xml
<table name="author">
  <column name="firstName"/>
  <column name="lastName"/>
  <column name="birthDate"/>
  <unique name="ix_first_name_last_name_date">
    <unique-column name="firstName"/>
    <unique-column name="lastName"/>
    <unique-column name="birthDate"/>
  </unique>
</table>
~~~