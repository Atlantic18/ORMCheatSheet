Configure `app/config/config.yml` and add Doctrine section:

~~~yaml
doctrine:
    dbal:
        driver:   %database_driver%
        host:     %database_host%
        port:     %database_port%
        dbname:   %database_name%
        user:     %database_user%
        password: %database_password%
        charset:  UTF8

    orm:
        auto_generate_proxy_classes: %kernel.debug%
        auto_mapping: true
~~~

Configure `app/config/parameters.yml` and set database connection parameters:

~~~yaml
parameters:
    database_driver:   pdo_mysql
    database_host:     127.0.0.1
    database_port:     ~
    database_name:     symfony
    database_user:     UsernameHere
    database_password: PasswordHere
~~~