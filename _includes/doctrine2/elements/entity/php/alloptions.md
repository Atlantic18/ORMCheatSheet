~~~php
<?php
use Doctrine\ORM\Mapping AS ORM;

/**
 * 
 * @ORM\Table(
 *     schema="item_record",
 *     name="item_record",
 *     options={
 *         "charset":"utf8",
 *         "collate":"utf8_unicode_ci",
 *         "comment":"library record of a work",
 *         "temporary":false,
 *         "engine":"InnoDB"
 *     },
 *     indexes={
 *         @ORM\Index(name="ix_name", columns={"itemRecord_name"}),
 *         @ORM\Index(name="ix_name_publisher", columns={"itemRecord_publisherId","itemRecord_name"})
 *     },
 *     uniqueConstraints={
 *         @ORM\UniqueConstraint(name="ix_name_ean", columns={"itemRecord_name","eanId"}),
 *         @ORM\UniqueConstraint(name="ix_ean_publisher", columns={"itemRecord_publisherId","eanId"})
 *     }
 * )
 * @ORM\DiscriminatorMap(
 *     {"itemRecord"="itemRecord","book"="book","magazine"="magazine","audioRecord"="audioRecord"}
 * )
 * @ORM\DiscriminatorColumn(name="item", type="string")
 * @ORM\InheritanceType("JOINED")
 * 
 * 
 * 
 * @ORM\HasLifecycleCallbacks
 * @ORM\ChangeTrackingPolicy("DEFERRED_IMPLICIT")
 * @ORM\Entity(repositoryClass="Doctrine\ORM\EntityRepository")
 */
class itemRecord
{
    /**
     * @ORM\Id
     * @ORM\Column()
     */
    private $id;

    /**
     * @ORM\Column()
     */
    private $name;

    /**
     * @ORM\OneToOne()
     */
    private $ean;

    /**
     * @ORM\OneToMany()
     */
    private $physicalCopy;

    /**
     * @ORM\ManyToOne()
     * @ORM\JoinColumn()
     */
    private $publisher;

    /**
     * @ORM\ManyToMany()
     */
    private $author;

    /**
     * @ORM\PostPersist
     */
    public function sendOptinMail()
    {
    }
}
~~~