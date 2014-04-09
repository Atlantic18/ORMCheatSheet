Modify `bootstrap.php` to use the MySQL database:

~~~
// bootstrap.php
$conn = Doctrine_Manager::connection('mysql://root:mys3cr3et@localhost/doctrinetest', 'doctrine');
~~~

You can use the <code>:php:meth:`$conn->createDatabase`</code> method to create the database if it does not already exist.

Storage file for created models:

~~~
mkdir doctrine_example/models
~~~
Generate models using PHP script:

~~~php
// test.php
Doctrine_Core::generateModelsFromDb(
    'models',
    array('doctrine'),
    array('generateTableClasses' => true)
);
~~~
You can place custom functions inside the classes to customize the functionality of your models. Below are some examples:

~~~php
// models/User.php
class User extends BaseUser
{
    public function setPassword($password)
    {
        return $this->_set('password', md5($password));
    }
}
~~~

In order for the above password accessor overriding to work properly you must enable the auto_accessor_override attribute in your bootstrap.php file like done below:

~~~php
// bootstrap.php
$manager->setAttribute(Doctrine_Core::ATTR_AUTO_ACCESSOR_OVERRIDE, true);
~~~
Now when you try and set a users password it will be md5 encrypted. 

###Autoload models from directory

~~~php
// bootstrap.php
Doctrine_Core::loadModels('models');
~~~

### Generate Schema Files from Models

Use PHP script:

~~~PHP
// example.php
Doctrine_Core::generateYamlFromModels('schema.yml', 'models');
~~~
Execute the example.php script:

~~~
php example.php
~~~

File named schema.yml is created in the root of the project directory.