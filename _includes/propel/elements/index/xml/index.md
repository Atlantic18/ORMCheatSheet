~~~xml
<table name="author">
  <column name="firstName"/>
  <column name="lastName"/>
  <index name="ix_name_last">
    <index-column name="lastName"/>
  </index>
</table>
~~~