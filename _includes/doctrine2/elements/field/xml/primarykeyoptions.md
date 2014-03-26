~~~xml
<id name="id" type="integer" length="255" column="itemRecord_id" 
column-definition="itemRecord_id" precision="3" scale="3" version="true">
  <generator strategy="SEQUENCE"/>
  <sequence-generator 
  allocation-size="1" 
  initial-value="1" 
  sequence-name="itemRecord_id_seq"/>
  <options>
    <option name="unsigned" value="true"/>
    <option name="comment" value="this is primary key"/>
    <option name="version" value="2"/>
  </options>
</id>
~~~
