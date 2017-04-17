For installation with Symfony 2.1 and newer select one ofthe following methods:

#### Dependencies and bin/vendors

Add the following snippets to "deps" files:

~~~
    [doctrine-mongodb]
        git=http://github.com/doctrine/dbal.git

    [doctrine-mongodb-odm]
        git=http://github.com/doctrine/doctrine2.git

    [DoctrineBundle]
        git=http://github.com/doctrine/DoctrineBundle.git
        target=/bundles/Doctrine/Bundle/DoctrineBundle
~~~

#### Composer

Add the following dependencies to your projects composer.json file:

~~~json
    "require": {
        # ..
        "doctrine/doctrine-bundle": "~1.2"
        # ..
    }
~~~    