~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<doctrine-mapping 
 xmlns="http://doctrine-project.org/schemas/orm/doctrine-mapping"
 xmlns:gedmo="http://gediminasm.org/schemas/orm/doctrine-extensions-mapping">
  <entity name="Entity\Item" table="items">
    <id name="id" type="integer" column="id">
      <generator strategy="AUTO"/>
    </id>

    <field name="name" type="string" length="128">
    </field>

    <field name="position" type="integer">
      <gedmo:sortable-position/>
    </field>
    <field name="category" type="string" length="128">
      <gedmo:sortable-group />
    </field>
  </entity>
</doctrine-mapping>
~~~