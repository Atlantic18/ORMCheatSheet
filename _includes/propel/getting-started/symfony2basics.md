####Database manipulation

Create a database:

~~~
> php app/console propel:database:create [--connection[=""]]
~~~

Drop a database:

~~~
> php app/console propel:database:drop [--connection[=""]] [--force]
~~~

####Migrations

Generates SQL diff between the XML schemas and the current database structure:

~~~
> php app/console propel:migration:generate-diff
~~~

Executes the migrations:

~~~
> php app/console propel:migration:migrate
~~~

Executes the next migration up:

~~~
> php app/console propel:migration:migrate --up
~~~

Executes the previous migration down:

~~~
> php app/console propel:migration:migrate --down
~~~

Lists the migrations yet to be executed:

~~~
> php app/console propel:migration:status
~~~

####Table Manipulations

You can drop one or several tables:

~~~
> php app/console propel:table:drop [--force] [--connection[="..."]] [table1] ... [tableN]
~~~

####Working with existing databases

Run the following command to generate an XML schema from your default database:

~~~
> php app/console propel:reverse
~~~

You can define which connection to use:

~~~
> php app/console propel:reverse --connection=default
~~~

This will create your schema file under `app/propel/generated-schemas`. 

####The Fixtures

Loading Fixtures:

~~~
> php app/console propel:fixtures:load [-d|--dir[="..."]] [--xml] [--sql] [--yml] [--connection[="..."]] [bundle]
~~~

You can pass a bundle name to load fixtures from it:

~~~
> php app/console propel:fixtures:load @AcmeDemoBundle
~~~