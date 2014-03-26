~~~php
/**
 * @ORM\Entity
 */
class itemRecord
{
    /**
     * @ORM\Column(
     *     type="string",
     *     length=255,
     *     nullable=false,
     *     name="itemRecord_name",
     *     columnDefinition="itemRecord_name",
     *     precision=1,
     *     scale=1,
     *     options={"comment":"this is field","unsigned":true,"version":3}
     * )
     */
    private $item;
}    
~~~
