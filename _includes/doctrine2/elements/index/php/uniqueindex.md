~~~php
/**
 * @ORM\Entity
 * @ORM\Table(
 *     uniqueConstraints={@ORM\UniqueConstraint(name="ix_first_name_last_name_date", columns={"firstName","lastName","birthDate"})}
 * )
 */
class author
~~~
