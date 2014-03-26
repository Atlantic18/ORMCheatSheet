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
     *     referencedColumnName="publisher_id",
     *     nullable=false
     * )
     */
    private $publisher;
}
~~~
