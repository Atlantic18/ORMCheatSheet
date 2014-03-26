```yaml
---
Entity\Category:
  type: entity
  repositoryClass: Gedmo\Tree\Entity\Repository\NestedTreeRepository
  table: categories
  gedmo:
    tree:
      type: nested
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    title:
      type: string
      length: 64
    lft:
      type: integer
      gedmo:
        - treeLeft
    rgt:
      type: integer
      gedmo:
        - treeRight
    root:
      type: integer
      nullable: true
      gedmo:
        - treeRoot
    lvl:
      type: integer
      gedmo:
        - treeLevel
  manyToOne:
    parent:
      targetEntity: Entity\Category
      inversedBy: children
      joinColumn:
        name: parent_id
        referencedColumnName: id
        onDelete: CASCADE
      gedmo:
        - treeParent
  oneToMany:
    children:
      targetEntity: Entity\Category
      mappedBy: parent
      orderBy:
        lft: ASC
```