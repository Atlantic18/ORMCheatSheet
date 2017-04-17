#### Composer

Create a new `composer.json` file at the root of your project's directory:

~~~json
{
    "require": {
        "propel/propel": ">= 2.0"
    }
}
~~~

Download Composer:

~~~
$ wget http://getcomposer.org/composer.phar
# If you haven't wget on your computer
$ curl -s http://getcomposer.org/installer | php
~~~

Install dependencies:

~~~
$ php composer.phar install
~~~

#### Git

~~~
$ git clone git://github.com/propelorm/Propel2 vendor/propel
~~~

To update Propel:

~~~
$ cd myproject/vendor/propel
$ git pull
~~~

#### Tarball

~~~
$ cd myproject/vendor
$ wget http://files.propelorm.org/propel-2.0.0.tar.gz
$ tar zxvf propel-2.0.0.tar.gz
$ mv propel-2.0.0 propel
~~~
