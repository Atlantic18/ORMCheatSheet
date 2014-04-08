You can use annotations for schema definition. Entities can be stored at `src\Acme\SampleBundle\Entity\User.php`:

~~~php
<?php
namespace Acme\SampleBundle\Entity;
use Doctrine\ORM\Mapping AS ORM;

/** 
 * @ORM\Entity
 * @ORM\Table(name="acme_user")
 */
class Event
{
    /** 
     * @ORM\Id
     * @ORM\Column(type="integer")
     * @ORM\GeneratedValue(strategy="AUTO")
     */
    private $id;

    /** 
     * @ORM\Column(type="string", unique=true, length=64, nullable=false)
     */
    private $name;
}
~~~

Getters and setters can be generated simply by running:

~~~
php app/console doctrine:generate:entities Acme
~~~