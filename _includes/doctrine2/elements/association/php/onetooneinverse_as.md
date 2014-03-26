~~~php
/**
 * @ORM\Entity
 */
class ean
{
    /**
     * @ORM\Id
     * @ORM\Column(type="integer")
     * @ORM\GeneratedValue(strategy="AUTO")
     */
    private $id;

    /**
     * @ORM\OneToOne(
     *     targetEntity="itemRecord",
     *     mappedBy="ean"
     * )
     */
    private $itemRecord;
}
~~~
