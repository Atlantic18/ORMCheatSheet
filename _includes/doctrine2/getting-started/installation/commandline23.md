~~~PHP
<?php
// cli-config.php
require_once 'my_bootstrap.php';

// Any way to access the EntityManager from  your application
$em = GetMyEntityManager();

$helperSet = new \Symfony\Component\Console\Helper\HelperSet(array(
    'db' => new \Doctrine\DBAL\Tools\Console\Helper\ConnectionHelper($em->getConnection()),
    'em' => new \Doctrine\ORM\Tools\Console\Helper\EntityManagerHelper($em)
));
~~~
