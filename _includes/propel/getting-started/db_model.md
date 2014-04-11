Go to the project directory anywhere on your filesystem:

~~~
$ cd MyProject
~~~

Run the `reverse` task to generate the `schema.xml` specifying your database credentials:

~~~
$ propel reverse "mysql:host=localhost;dbname=db;user=root;password=pwd"
~~~

Now you have a `schema.xml` file in the MyProject/ project directory. 
