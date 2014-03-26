```PHP
<?php
namespace Entity;

use Gedmo\Mapping\Annotation as Gedmo;
use Doctrine\ORM\Mapping as ORM;

/**
 * @ORM\Table(name="articles")
 * @ORM\Entity
 */
class Article
{
    /**
     * @ORM\Id
     * @ORM\GeneratedValue
     * @ORM\Column(type="integer")
     */
    private $id;

    /**
     * @ORM\Column(length=64)
     */
    private $title;

    /**
     * @ORM\Column(length=16)
     */
    private $code;

    /**
     * @Gedmo\Slug(fields={"title", "code"})
     * @ORM\Column(length=128, unique=true)
     */
    private $slug;

    public function getId()
    {
        return $this->id;
    }

    public function setTitle($title)
    {
        $this->title = $title;
    }

    public function getTitle()
    {
        return $this->title;
    }

    public function setCode($code)
    {
        $this->code = $code;
    }

    public function getCode()
    {
        return $this->code;
    }

    public function getSlug()
    {
        return $this->slug;
    }
}
```