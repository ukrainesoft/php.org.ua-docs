---
navigation:
  - class.xmldiff-file.html: « XMLDiffFile
  - xmldiff-file.merge.html: 'XMLDiffFile::merge »'
  - index.html: PHP Manual
  - class.xmldiff-file.html: XMLDiffFile
title: 'XMLDiffFile::diff'
---
# XMLDiffFile::diff

(PECL xmldiff >= 0.8.0)

XMLDiffFile::diff — Порівняння двох файлів XML

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
