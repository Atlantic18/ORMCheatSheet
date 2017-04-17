#### Writing Data Fixtures

The times of using YAML for data fixtures is no longer. Instead, you are only required to use plain PHP for loading your data fixtures.

~~~
// data/fixtures/fixtures.php
 
$em = $this->getEntityManager();
 
$admin = new \Models\User();
$admin->username = 'admin';
$admin->password = 'changeme';
~~~

#### Building Doctrine

Now you're ready to build everything. The following command will build models, forms, filters, database and load data fixtures.

~~~
$ php symfony doctrine:build --all --and-load
~~~

#### Updating Schema

If you change your schema mapping information and want to update the database you can easily do so by running the following command after changing your mapping information.

~~~
$ php symfony doctrine:build --all-classes --and-update-schema
~~~
