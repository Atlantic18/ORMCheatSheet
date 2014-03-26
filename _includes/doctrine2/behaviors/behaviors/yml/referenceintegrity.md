```YAML
---
Document\Type:
  type: document
  collection: types
  fields:
      id:
          id:     true
      title:
          type:   string
      article:
          reference: true
          type: one
          mappedBy: type
          targetDocument: Document\Article
          gedmo:
              referenceIntegrity: nullify   # or restrict
```