~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<doctrine-mapping 
 xmlns="http://doctrine-project.org/schemas/orm/doctrine-mapping"
 xmlns:gedmo="http://gediminasm.org/schemas/orm/doctrine-extensions-mapping">
  <entity name="Entity\Article" table="sluggables">
    <id name="id" type="integer" column="id">
      <generator strategy="AUTO"/>
    </id>

    <field name="title" type="string" length="128"/>
    <field name="code" type="string" length="16"/>
    <field name="ean" type="string" length="13"/>
    <field name="slug" type="string" length="156" unique="true">
      <gedmo:slug unique="true" style="camel" updatable="false" separator="_" fields="title,code,ean" />
    </field>
  </entity>
</doctrine-mapping>
~~~