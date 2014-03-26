~~~yaml
  actAs:
     Blameable:
      columns:
        created:
          disabled: false
          length: 8
          name: created_by
          alias: alias
          type: integer
        updated:
          alias: alias
          disabled: false
          length: 8
          name: updated_by
          onInsert: true
          type: integer
      blameVar: userId
      default: false
      listener: Doctrine_Template_Listener_Blameable
      relations:
        created:
          class: User
          disabled: true
          foreign: id
          name: CreatedBy
        updated:
          class: User
          disabled: true
          foreign: id
          name: UpdatedBy
~~~