~~~yaml
author:
  type: entity
  fields:
    id:
      id: true
      type: integer
      generator:
        strategy: AUTO
    firstName:
      type: string
      nullable: false
    lastName:
      type: string
      nullable: false
    birthDate:
      type: string
      nullable: true
~~~
