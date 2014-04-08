Add required bundles to composer.json:
~~~json
    "require": {
        ....
        ....
        "doctrine/orm": "*",
        "doctrine/doctrine-bundle": "*",
    },
~~~

And enable the bundles in the Kernel:

~~~json
class AppKernel extends Kernel
{
    public function registerBundles()
    {
        $bundles = array(
            .......
            new Doctrine\Bundle\DoctrineBundle\DoctrineBundle(),
        );

        .....

        return $bundles;
    }
}
~~~