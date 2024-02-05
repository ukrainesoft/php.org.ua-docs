---
navigation:
  - class.xmldiff-file.md: « XMLDiff\\File
  - xmldiff-file.merge.md: 'XMLDiff\\File::merge »'
  - index.md: PHP Manual
  - class.xmldiff-file.md: XMLDiff\\File
title: 'XMLDiff\\File::diff'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\File::diff

(PECL xmldiff >= 0.8.0)

XMLDiff\\File::diff — Порівняння двох файлів XML

### Опис

```methodsynopsis
public XMLDiff\File::diff(string $from, string $to): string
```

Порівнює два локальні файли XML і повертає рядок з інформацією про відмінності.

### Список параметрів

`from`

Шлях до джерела документа.

`to`

Шлях до цільового документа.

### Значення, що повертаються

Рядок з XML-документом, що містить інформацію про відмінності, або **`null`**
