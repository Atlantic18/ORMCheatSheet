Autoloading is taken care of by Composer. You just have to include the composer autoload file in your project:
~~~PHP
<?php
// bootstrap.php
// Include Composer Autoload (relative to project root).
require_once "vendor/autoload.php";
~~~
