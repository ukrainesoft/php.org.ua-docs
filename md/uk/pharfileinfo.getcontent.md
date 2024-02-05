---
navigation:
  - pharfileinfo.getcompressedsize.md: '« PharFileInfo::getCompressedSize'
  - pharfileinfo.getmetadata.md: 'PharFileInfo::getMetadata »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::getContent'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharFileInfo::getContent

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

PharFileInfo::getContent — Отримати повний вміст файлу запису

### Опис

```methodsynopsis
public PharFileInfo::getContent(): string
```

Ця функція поводиться як [file\_get\_contents()](function.file-get-contents.md)але для Phar.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст файлу.
