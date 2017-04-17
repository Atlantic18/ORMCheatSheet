Configure `config/databases.yml` for database connection:

~~~yaml
all:
  doctrine:
    class: sfDoctrineDatabase
    param:
      options:
        driver: pdo_mysql
        user: root
        password:
        dbname: doctrine
~~~

#### Configure Your Schema

Below is an example of a simple User entity:

~~~yaml
# config/doctrine/schema.yml
 
Models\User:
  type: entity
  table: user
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    username:
      type: string
      length: 255
    password:
      type: string
      length: 255
~~~
