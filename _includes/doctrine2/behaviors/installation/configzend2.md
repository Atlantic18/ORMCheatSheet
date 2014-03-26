Declaring appropriate subscribers in Event Manager settings. With [entity mapping options](https://github.com/doctrine/DoctrineORMModule#entities-settings) module configuration file should look like this:

```php
return array(
    'doctrine' => array(
        'eventmanager' => array(
            'orm_default' => array(
                'subscribers' => array(
                
                    // pick any listeners you need
                    'Gedmo\Tree\TreeListener',
                    'Gedmo\Timestampable\TimestampableListener',
                    'Gedmo\Sluggable\SluggableListener',
                    'Gedmo\Loggable\LoggableListener',
                    'Gedmo\Sortable\SortableListener'
                ),
            ),
        ),
        'driver' => array(
            'my_driver' => array(
                'class' => 'Doctrine\ORM\Mapping\Driver\AnnotationDriver',
                'cache' => 'array',
                'paths' => array(__DIR__ . '/../src/MyModule/Entity')
            ),
            'orm_default' => array(
                'drivers' => array(
                    'MyModule\Entity' => 'my_driver'
                ),
            ),
        ),
    ),
);
```