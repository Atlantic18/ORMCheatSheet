~~~xml
<entity name="library\itemRecord" 
inheritance-type="JOINED" 
change-tracking-policy="DEFERRED_IMPLICIT" 
repository-class="Doctrine\ORM\EntityRepository" 
schema="item_record" table="item_record">
    <id name="id"/>
    <field name="name"/>
    <indexes/>
    <unique-constraints/>
    <lifecycle-callbacks/>
    <many-to-one field="publisher"/>
    <one-to-one field="ean"/>
    <one-to-many field="physicalCopy"/>
    <many-to-many field="author"/>
    <discriminator-column name="item"/>
    <discriminator-map/>
    <options>
      <option name="charset" value="utf8"/>
      <option name="collate" value="utf8_unicode_ci"/>
      <option name="comment" value="library record of a work"/>
      <option name="temporary" value="false"/>
      <option name="engine" value="InnoDB"/>
    </options>
  </entity>
</doctrine-mapping>
~~~
