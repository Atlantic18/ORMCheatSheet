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
     *     name="itemRecord_id"
     *     length=255     
     * )
     * @ORM\GeneratedValue(strategy="AUTO")
     */
    private $id;
~~~
