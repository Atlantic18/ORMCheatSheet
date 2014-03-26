```yaml
---
Entity\File:
  type: entity
  table: files
  gedmo:
    uploadable:
      allowOverwrite: true
      appendNumber: true
      path: '/my/path'
      pathMethod: getPath
      callback: callbackMethod
      filenameGenerator: SHA1
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    path:
      type: string
      gedmo:
        - uploadableFilePath
    path:
      type: string
      gedmo:
        - uploadableFileName
    mimeType:
      type: string
      gedmo:
        - uploadableFileMimeType
    size:
      type: decimal
      gedmo:
        - uploadableFileSize
```