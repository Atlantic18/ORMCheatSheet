~~~xml
<field name="item" type="string" length="255" nullable="false" column="itemRecord_name" column-definition="itemRecord_name" precision="1" scale="1" version="false">
  <generator>
    <strategy>UUID</strategy>
  </generator>
  <sequence-generator>
    <allocation-size>2</allocation-size>
    <initial-value>1</initial-value>
    <sequence-name>itemRecord_name_seq</sequence-name>
  </sequence-generator>
  <options>
    <option name="comment" value="this is field"/>
    <option name="unsigned" value="true"/>
    <option name="version" value="3"/>
  </options>
</field>
~~~
