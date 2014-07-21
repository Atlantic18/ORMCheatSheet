~~~php
<?php
$paths = array("/path/to/yml-mappings");
$config = Setup::createYAMLMetadataConfiguration($paths, $isDevMode);
$entityManager = EntityManager::create($dbParams, $config);
~~~
