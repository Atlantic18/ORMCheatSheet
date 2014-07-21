~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<doctrine-mapping 
 xmlns="http://doctrine-project.org/schemas/orm/doctrine-mapping"
 xmlns:gedmo="http://gediminasm.org/schemas/orm/doctrine-extensions-mapping">

  <entity 
   name="Mapping\Fixture\Xml\Translatable" 
   table="translatables">

    <id name="id" type="integer" column="id">
      <generator strategy="AUTO"/>
    </id>

    <field name="title" type="string" length="128">
      <gedmo:translatable/>
    </field>
    <field name="content" type="text">
      <gedmo:translatable/>
    </field>

    <gedmo:translation 
     entity="Gedmo\Translatable\Entity\Translation" 
     locale="locale"/>

  </entity>

</doctrine-mapping>
~~~