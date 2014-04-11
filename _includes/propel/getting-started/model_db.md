####Set Up Build Configuration

Propel expects the build configuration to be stored in a file called `build.properties`, and stored at the same level as the `schema.xml`. Here is an example for a MySQL database:

~~~
# Database driver
propel.database = mysql

# Project name
propel.project = MyProject
~~~

####Use the propel Script To Build The SQL Code

~~~
$ cd /path/to/my/project
$ propel sql:build
~~~

####Generate Model Classes

~~~
$ propel model:build
~~~