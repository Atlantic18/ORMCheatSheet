~~~
php composer.phar require doctrine/doctrine-orm-module:0.7.*
~~~
~~~
php composer.phar require zendframework/zend-developer-tools:dev-master
~~~
~~~
cp vendor/zendframework/zend-developer-tools/config/zenddevelopertools.local.php.dist config/autoload/zdt.local.php
~~~
Enable the modules in `config/application.config.php`:
~~~PHP
return array(
    'modules' => array(
        'ZendDeveloperTools',
        'DoctrineModule',
        'DoctrineORMModule',
        'Application',
    ),
    // [...]
);
~~~
