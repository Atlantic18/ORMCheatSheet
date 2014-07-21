~~~php
<?php
namespace Document;

use Doctrine\ODM\MongoDB\Mapping\Annotations as ODM;
use Gedmo\Mapping\Annotation as Gedmo;

/**
 * @ODM\Document(collection="types")
 */
class Type
{
    /**
     * @ODM\Id
     */
    private $id;

    /**
     * @ODM\String
     */
    private $title;

    /**
     * @ODM\ReferenceOne(targetDocument="Article", mappedBy="type")
     * @Gedmo\ReferenceIntegrity("nullify")
     * @var Article
     */
    protected $article;

    // ...
}
~~~