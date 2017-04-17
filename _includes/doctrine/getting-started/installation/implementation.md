###Include Doctrine libraries

Find the `Doctrine.php` file containing the core class in the lib folder where you downloaded Doctrine.

Move doctrine libraries to a folder in your project:

~~~
mkdir lib
mkdir lib/vendor
mkdir lib/vendor/doctrine
mv /path/to/doctrine/lib doctrine
~~~

Or you can use externals:

~~~
svn co http://svn.doctrine-project.org/branches/1.2/lib lib/vendor/doctrine
~~~

Add it to your svn externals:

~~~
svn propedit svn:externals lib/vendor
~~~
This will open up your editor. Place the following inside and save:

~~~
doctrine http://svn.doctrine-project.org/branches/1.2/lib
~~~

When you do SVN update you will get the Doctrine libraries updated:

~~~
svn update lib/vendor
~~~

###Require Doctrine Base Class

Create a file named `bootstrap.php` and place the following code in the file:

~~~php
// bootstrap.php
/* Bootstrap Doctrine.php, register autoloader specify
   configuration attributes and load models. */

require_once(dirname(**FILE**) . '/lib/vendor/doctrine/Doctrine.php');
~~~

###Register Autoloader

Register the class <code>:php:class:`Doctrine`</code> autoloader function in the bootstrap file:

~~~php
// bootstrap.php
spl_autoload_register(array('Doctrine', 'autoload'));

~~~

Create the singleton <code>:php:class:`Doctrine_Manager`</code> instance and assign it to a variable named `$manager`:

~~~php
// bootstrap.php
$manager = Doctrine_Manager::getInstance();
~~~