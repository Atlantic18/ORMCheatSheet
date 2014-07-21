~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<doctrine-mapping 
 xmlns="http://doctrine-project.org/schemas/orm/doctrine-mapping"
 xmlns:gedmo="http://gediminasm.org/schemas/orm/doctrine-extensions-mapping">

  <entity name="Mapping\Fixture\Xml\Blameable" table="blameables">
    <id name="id" type="integer" column="id">
      <generator strategy="AUTO"/>
    </id>

    <field name="createdBy" type="string">
      <gedmo:blameable on="create"/>
    </field>
    <field name="updatedBy" type="string">
      <gedmo:blameable on="update"/>
    </field>
    <field name="publishedBy" type="string" nullable="true">
      <gedmo:blameable on="change" field="status.title" value="Published"/>
    </field>

    <many-to-one field="status" target-entity="Status">
      <join-column name="status_id" referenced-column-name="id"/>
    </many-to-one>
  </entity>

</doctrine-mapping>
~~~