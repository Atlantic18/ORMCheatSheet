~~~PHP
<?php
namespace Entity;

use Gedmo\Mapping\Annotation as Gedmo;
use Doctrine\ORM\Mapping as ORM;

/**
 * @ORM\Entity
 * @Gedmo\Uploadable(path="/my/path", callback="myCallbackMethod", filenameGenerator="SHA1", allowOverwrite=true, appendNumber=true)
 */
class File
{
    /**
     * @ORM\Column(name="id", type="integer")
     * @ORM\Id
     * @ORM\GeneratedValue(strategy="IDENTITY")
     */
    private $id;

    /**
     * @ORM\Column(name="path", type="string")
     * @Gedmo\UploadableFilePath
     */
    private $path;

    /**
     * @ORM\Column(name="name", type="string")
     * @Gedmo\UploadableFileName
     */
    private $name;

    /**
     * @ORM\Column(name="mime_type", type="string")
     * @Gedmo\UploadableFileMimeType
     */
    private $mimeType;

    /**
     * @ORM\Column(name="size", type="decimal")
     * @Gedmo\UploadableFileSize
     */
    private $size;


    public function myCallbackMethod(array $info)
    {
        // Do some stuff with the file..
    }

    // Other methods..
}
~~~