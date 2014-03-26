~~~yaml
library\itemRecord:
  type: entity
  inheritanceType: JOINED
  changeTrackingPolicy: DEFERRED_IMPLICIT
  repositoryClass: Doctrine\ORM\EntityRepository
  schema: item_record
  table: item_record
  fields:
  indexes:
  uniqueConstraints:
  lifecycleCallbacks:
  options:
    charset: utf8
    collate: utf8_unicode_ci
    comment: library record of a work
    temporary: false
    engine: InnoDB
  oneToOne:
  oneToMany:
  manyToOne:
  manyToMany:
  discriminatorColumn:
  discriminatorMap:
~~~
