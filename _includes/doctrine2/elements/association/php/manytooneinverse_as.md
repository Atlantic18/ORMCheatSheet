~~~php
/**
 * @ORM\Entity
 */
class publisher
{
    /**
     * @ORM\Id
     */
    private $id;

    /**
     * @ORM\OneToMany(
     *     targetEntity="itemRecord",
     *     mappedBy="publisher"
     * )
     */
    private $itemRecord;
}
~~~
