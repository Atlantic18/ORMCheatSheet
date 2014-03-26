Install [Symfony-standard edition
with composer](http://github.com/KnpLabs/symfony-with-composer):

- `git clone git://github.com/KnpLabs/symfony-with-composer.git example`
- `cd example && rm -rf .git && php bin/vendors install`
- ensure your application [loads and meets requirements](http://your_virtual_host/app_dev.php)

Add the **gedmo/doctrine-extensions** into **composer.json**

```JSON
{
    "require": {
        "php":              ">=5.3.2",
        "symfony/symfony":  ">=2.0.9,<2.1.0-dev",
        "doctrine/orm":     ">=2.1.0,<2.2.0-dev",
        "twig/extensions":  "*",

        "symfony/assetic-bundle":         "*",
        "sensio/generator-bundle":        "2.0.*",
        "sensio/framework-extra-bundle":  "2.0.*",
        "sensio/distribution-bundle":     "2.0.*",
        "jms/security-extra-bundle":      "1.0.*",
        "gedmo/doctrine-extensions":      "dev-master"
    },

    "autoload": {
        "psr-0": {
            "Acme": "src/"
        }
    }
}
```

Update vendors: `php composer.phar update gedmo/doctrine-extensions`
Configure your database connection parameters: `app/config/parameters.ini`