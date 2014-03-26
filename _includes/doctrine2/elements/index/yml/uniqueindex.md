```YAML
author:
  type: entity
  fields:
    firstName:
    lastName:
    birthDate:
  uniqueConstraints:
    ix_first_name_last_name_date:
      columns: [firstName, lastName, birthDate]
```
