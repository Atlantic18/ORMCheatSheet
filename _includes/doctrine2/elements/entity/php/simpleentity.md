~~~php
<?php
use Doctrine\ORM\Mapping AS ORM;

/**
 * @ORM\Entity
 */
class author
{
    /**
     * @ORM\Id
     * @ORM\Column(type="integer")
     * @ORM\GeneratedValue(strategy="AUTO")
     */
    private $id;

    /**
     * @ORM\Column(type="string", nullable=false)
     */
    private $firstName;

    /**
     * @ORM\Column(type="string", nullable=false)
     */
    private $lastName;

    /**
     * @ORM\Column(type="string", nullable=true)
     */
    private $birthDate;
~~~
