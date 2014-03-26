~~~php
/**
 * @ORM\Entity
 */
class itemRecord
{
    /**
     * @ORM\ManyToOne(
     *     targetEntity="publisher",
     *     inversedBy="itemRecord",
     *     fetch="EXTRA_LAZY",
     *     orphanRemoval=true,
     *     cascade={"all","merge","persist","refresh","remove"}
     * )
     * @ORM\JoinColumn(
     *     name="publisherId",
     *     referencedColumnName="publisher_id",
     *     nullable=false,
     *     columnDefinition="itemRecord_publisherId",
     *     onDelete="CASCADE",
     *     onUpdate="RESTRICT"
     * )
     */
    private $publisher;
}
~~~
