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
     * @ORM\ManyToMany(targetEntity="itemRecord", inversedBy="author", cascade={"all","refresh"})
     * @ORM\JoinTable(
     *     name="itemRecordHasAuthor",
     *     joinColumns={
     *         @ORM\JoinColumn(
     *             name="authorId",
     *             referencedColumnName="id",
     *             nullable=false,
     *             fetch="EAGER",
     *             onDelete="CASCADE",
     *             onUpdate="RESTRICT"
     *         )
     *     },
     *     inverseJoinColumns={@ORM\JoinColumn(name="bookId", referencedColumnName="itemRecord_id", nullable=false)}
     * )
     * @ORM\OrderBy({"id"="ASC"})
     */
    private $itemRecord;
}
~~~
