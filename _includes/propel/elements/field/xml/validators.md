~~~xml
<column name="item" type="Varchar"/>
<validator column="item">
  <rule name="/validator class/" value="/value/" message="/custom message/"/>
  <rule name="match" value="/regexp/" message="Does match the regexp"/>
  <rule name="maxLength" value="1024" message="exceeded maxlenght"/>
  <rule name="maxValue" value="1025" message="exceeded max value"/>
  <rule name="minLength" value="4" message="shorter than min lenght"/>
  <rule name="minValue" value="5" message="smaller than min value"/>
  <rule name="notMatch" value="/regexp/" message="does not match the regexp"/>
  <rule name="/validator name/" value="/use this for other propel validators/" message="/custom message/"/>
  <rule name="required" message="column is required"/>
  <rule name="type" value="integer" message="wrong type"/>
  <rule name="unique" message="not unique"/>
  <rule name="validValues" value="book|magazine" message="is valid value"/>
</validator>
~~~