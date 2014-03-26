~~~php
/**
 * @ORM\Entity
 * @ORM\InheritanceType("JOINED")
 * @ORM\DiscriminatorColumn(name="item", type="string")
 * @ORM\DiscriminatorMap(
 *     {"itemRecord"="itemRecord","book"="book","magazine"="magazine","audioRecord"="audioRecord"}
 * )
 */
class itemRecord
~~~
