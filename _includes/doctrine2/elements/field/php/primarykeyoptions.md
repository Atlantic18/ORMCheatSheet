~~~php
/**
 * @ORM\Entity
 */
class itemRecord
{
    /**
     * @ORM\Id
     * @ORM\Column(
     *     type="integer",
     *     name="itemRecord_id",
     *     length=255
     *     columnDefinition="itemRecord_id",
     *     precision=3,
     *     scale=3,
     *     options={"unsigned":true,"comment":"this is primary key","version":2}
     * )
     * @ORM\Version
     * @ORM\GeneratedValue(strategy="SEQUENCE")
     */
    private $id;
~~~
