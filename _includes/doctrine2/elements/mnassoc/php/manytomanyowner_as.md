~~~php
/**
 * @ORM\Entity
 */
class itemRecord
{
    /**
     * @ORM\ManyToMany(targetEntity="author", mappedBy="itemRecord")
     */
    private $author;
}
~~~
