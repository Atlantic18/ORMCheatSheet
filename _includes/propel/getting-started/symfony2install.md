####Composer (recommended):

~~~json
{
    "require": {
        // ...
        "propel/propel-bundle": "1.2.*"
    }
}
Tip
~~~

Different bundle version may be needed for different Symfony2 version. Check PropelBundle for details.

####Git, SVN, Git submodules, or the Symfony vendor management (deps file):

Clone this bundle in the `vendor/bundles/Propel` directory:

~~~
> git submodule add https://github.com/propelorm/PropelBundle.git vendor/bundles/Propel/PropelBundle
~~~

Checkout Propel and Phing in the vendor directory:

~~~
> svn checkout http://svn.github.com/propelorm/Propel.git vendor/propel
> svn checkout http://svn.phing.info/tags/2.4.6/ vendor/phing
~~~

Instead of using svn, you can clone the unofficial Git repositories:

~~~
> git submodule add https://github.com/phingofficial/phing.git vendor/phing
~~~

~~~
> git submodule add https://github.com/propelorm/Propel.git vendor/propel
~~~

Instead of doing this manually, you can use the Symfony vendor management via the deps file. If you are using a Symfony2 2.x.x version (actually, a version which is not 2.1 or above), be sure to deps.lock the PropelBundle to a commit on the 2.0 branch, which does not use the Bridge

###Bundle registration

~~~php
<?php
public function registerBundles()
{
    $bundles = array(
        // ...
        new Propel\PropelBundle\PropelBundle(),
    );

    // ...
}
~~~

Register the PropelBundle namespace in `app/autoload.php` if you are not using Composer:

~~~php
<?php
$loader->registerNamespaces(array(
    // ...
    'Propel' => __DIR__.'/../vendor/bundles',
));
$loader->registerPrefixes(array(
    // ...
    'Phing'  => __DIR__.'/../vendor/phing/classes/phing',
));
~~~

Now, you can build your model classes, and SQL by running the following command:

~~~php
> php app/console propel:build [--classes] [--sql] [--insert-sql]
~~~

To insert SQL statements, use the propel:sql:insert command:

~~~php
> php app/console propel:sql:insert [--force]
~~~