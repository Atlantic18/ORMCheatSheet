~~~php
/**
 * @ORM\Entity
 */
class publisher
{
    /**
     * @ORM\Id
     * @ORM\Column(
     *     type="integer"
     * )
     * @ORM\GeneratedValue(strategy="SEQUENCE")
     */
    private $id;

    /**
     * @ORM\OneToMany(
     *     targetEntity="itemRecord",
     *     mappedBy="publisher",
     *     fetch="EAGER",
     *     indexBy="id",
     *     cascade={"all","merge","persist","refresh","remove"}
     * )
     * @ORM\OrderBy({"id"="ASC"})
     */
    private $itemRecord;
}
~~~
