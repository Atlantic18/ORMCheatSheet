~~~yaml
---
Entity\Article:
  type: entity
  table: articles
  gedmo:
    loggable:
# using specific personal LogEntryClass class:
      logEntryClass: My\LogEntry
# without specifying the LogEntryClass class:
#   loggable: true
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    title:
      type: string
      length: 64
      gedmo:
        - versioned
    content:
      type: text
~~~