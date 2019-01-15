~~~php
/**
 * @ORM\Entity
 */
class itemRecord
{
    /**
     * @ORM\ManyToOne(
     *     targetEntity="publisher",
     *     inversedBy="itemRecord"
     * )
     * @ORM\JoinColumn(
     *     name="publisherId",
     *     referencedColumnName="id",
     *     nullable=false
     * )
     */
    private $publisher;
}
~~~
