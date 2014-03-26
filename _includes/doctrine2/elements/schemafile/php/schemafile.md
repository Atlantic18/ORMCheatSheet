~~~php
<?php
use Doctrine\ORM\Mapping AS ORM;

/** 
 * @ORM\Entity(repositoryClass="Doctrine\ORM\EntityRepository")
 * @ORM\Table
 */
class itemRecord
{
    /** 
     * @ORM\Id
     */
    private $id;

    /** 
     * @ORM\Column
     */
    private $name;
~~~
