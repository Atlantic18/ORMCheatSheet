~~~php
<?php
$paths = array("/path/to/xml-mappings");
$config = Setup::createXMLMetadataConfiguration($paths, $isDevMode);
$entityManager = EntityManager::create($dbParams, $config);
~~~
