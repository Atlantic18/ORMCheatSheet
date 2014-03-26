To re-generate everything and make sure the database is reinstantiated each time prepare script:

```php
// generate.php
require_once('bootstrap.php');

Doctrine_Core::dropDatabases(); Doctrine_Core::createDatabases();
Doctrine_Core::generateModelsFromYaml('schema.yml', 'models');
Doctrine_Core::createTablesFromModels('models');
```

Regenerate the database from the schemafiles running the command:
```
php generate.php
```