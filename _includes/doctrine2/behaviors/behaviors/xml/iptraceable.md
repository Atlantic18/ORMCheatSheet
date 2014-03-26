```XML
<?xml version="1.0" encoding="UTF-8"?>
<doctrine-mapping 
 xmlns="http://doctrine-project.org/schemas/orm/doctrine-mapping"
 xmlns:gedmo="http://gediminasm.org/schemas/orm/doctrine-extensions-mapping">

  <entity name="Mapping\Fixture\Xml\IpTraceable" table="ip-traceable">
    <id name="id" type="integer" column="id">
      <generator strategy="AUTO"/>
    </id>

    <field name="createdFromIp" type="string", length="45", nullable="true">
      <gedmo:ip-traceable on="create"/>
    </field>
    <field name="updatedFromIp" type="string", length="45", nullable="true">
      <gedmo:ip-traceable on="update"/>
    </field>
    <field name="publishedFromIp" type="string" nullable="true", length="45">
      <gedmo:ip-traceable on="change" field="status.title" value="Published"/>
    </field>

    <many-to-one field="status" target-entity="Status">
      <join-column name="status_id" referenced-column-name="id"/>
    </many-to-one>
  </entity>

</doctrine-mapping>
```