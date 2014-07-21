~~~xml
<?xml version="1.0" encoding="UTF-8"?>
<doctrine-mapping 
 xmlns="http://doctrine-project.org/schemas/orm/doctrine-mapping"
 xmlns:gedmo="http://gediminasm.org/schemas/orm/doctrine-extensions-mapping">

  <entity name="Mapping\Fixture\Xml\NestedTree" 
   table="nested_trees" 
   repository-class="Gedmo\Tree\Entity\Repository\NestedTreeRepository">

    <indexes>
      <index name="name_idx" columns="name"/>
    </indexes>

    <id name="id" type="integer" column="id">
      <generator strategy="AUTO"/>
    </id>

    <field name="name" type="string" length="128"/>
    <field name="left" column="lft" type="integer">
      <gedmo:tree-left/>
    </field>
    <field name="right" column="rgt" type="integer">
      <gedmo:tree-right/>
    </field>
    <field name="root" type="integer" nullable="true">
      <gedmo:tree-root/>
    </field>
    <field name="level" column="lvl" type="integer">
      <gedmo:tree-level/>
    </field>

    <many-to-one 
     field="parent" 
     target-entity="NestedTree" 
     inversed-by="children">
      <join-column 
       name="parent_id" 
       referenced-column-name="id" 
       on-delete="CASCADE"/>
      <gedmo:tree-parent/>
    </many-to-one>

    <one-to-many field="children" target-entity="NestedTree" mapped-by="parent">
      <order-by>
        <order-by-field name="left" direction="ASC" />
      </order-by>
    </one-to-many>

    <gedmo:tree type="nested"/>

  </entity>

</doctrine-mapping>
~~~
