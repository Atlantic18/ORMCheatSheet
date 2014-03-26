```XML
<?xml version="1.0" encoding="UTF-8"?>

<doctrine-mapping 
 xmlns="http://doctrine-project.org/schemas/orm/doctrine-mapping"
 xmlns:gedmo="http://gediminasm.org/schemas/orm/doctrine-extensions-mapping">

  <entity name="Entity\File" table="files">

    <id name="id" type="integer" column="id">
      <generator strategy="AUTO"/>
    </id>

    <field name="mimeType" column="mime" type="string">
      <gedmo:uploadable-file-mime-type />
    </field>

    <field name="size" column="size" type="decimal">
      <gedmo:uploadable-file-size />
    </field>

    <field name="name" column="name" type="string">
      <gedmo:uploadable-file-name />
    </field>

    <field name="path" column="path" type="string">
      <gedmo:uploadable-file-path />
    </field>

    <gedmo:uploadable
      allow-overwrite="true"
      append-number="true"
      path="/my/path"
      path-method="getPath"
      callback="callbackMethod"
      filename-generator="SHA1" />

  </entity>

</doctrine-mapping>
```