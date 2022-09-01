---
navigation:
  - class.xmldiff-memory.html: « XMLDiffMemory
  - xmldiff-memory.merge.html: 'XMLDiffMemory::merge »'
  - index.md: PHP Manual
  - class.xmldiff-memory.html: XMLDiffMemory
title: 'XMLDiffMemory::diff'
---
# XMLDiffMemory::diff

(PECL xmldiff >= 0.8.0)

XMLDiffMemory::diff — Порівняння двох документів XML

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
