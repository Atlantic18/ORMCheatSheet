~~~php
/**
 * @ORM\Entity
 */
class author
{
    /**
     * @ORM\Id
     */
    private $id;

    /**
     * @ORM\ManyToMany(targetEntity="itemRecord", inversedBy="author")
     * @ORM\JoinTable(
     *     name="itemRecordHasAuthor",
     *     joinColumns={
     *         @ORM\JoinColumn(
     *             name="authorId",
     *             referencedColumnName="id",
     *             nullable=false
     *         )
     *     },
     *     inverseJoinColumns={@ORM\JoinColumn(name="bookId", referencedColumnName="itemRecord_id", nullable=false)}
     * )
     */
    private $itemRecord;
}
~~~
