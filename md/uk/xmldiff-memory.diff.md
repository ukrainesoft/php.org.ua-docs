---
navigation:
  - class.xmldiff-memory.md: « XMLDiff\\Memory
  - xmldiff-memory.merge.md: 'XMLDiff\\Memory::merge »'
  - index.md: PHP Manual
  - class.xmldiff-memory.md: XMLDiff\\Memory
title: 'XMLDiff\\Memory::diff'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\Memory::diff

(PECL xmldiff >= 0.8.0)

XMLDiff\\Memory::diff — Порівняння двох документів XML

### Опис

```methodsynopsis
public XMLDiff\Memory::diff(string $from, string $to): string
```

Порівнює два рядки з XML та повертає рядок з інформацією про відмінності.

### Список параметрів

`from`

XML-документ джерело.

`to`

Цільовий документ XML.

### Значення, що повертаються

Рядок з XML-документом, що містить інформацію про відмінності, або **`null`**
