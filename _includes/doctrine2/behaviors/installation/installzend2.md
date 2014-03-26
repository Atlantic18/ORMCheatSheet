Add DoctrineModule, DoctrineORMModule and DoctrineExtensions to composer.json file:

```json
{
    "require": {
        "php": ">=5.3.3",
        "zendframework/zendframework": "2.1.*",
        "doctrine/doctrine-module": "0.*",
        "doctrine/doctrine-orm-module": "0.*",
        "gedmo/doctrine-extensions": "2.3.*",
    }
}
```
    
Then run `composer.phar update`.
