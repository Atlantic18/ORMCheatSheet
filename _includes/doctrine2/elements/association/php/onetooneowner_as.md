~~~php
/**
 * @ORM\Entity
 */
class itemRecord
{
    /**
     * @ORM\OneToOne(
     *     targetEntity="ean",
     *     inversedBy="itemRecord"
     * )
     * @ORM\JoinColumn(name="eanId", referencedColumnName="id", unique=true)
     */
    private $ean;
}
~~~
