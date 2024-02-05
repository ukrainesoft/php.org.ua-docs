---
navigation:
  - xmldiff-dom.diff.md: '« XMLDiff\\DOM::diff'
  - class.xmldiff-memory.md: XMLDiff\\Memory »
  - index.md: PHP Manual
  - class.xmldiff-dom.md: XMLDiff\\DOM
title: 'XMLDiff\\DOM::merge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\DOM::merge

(PECL xmldiff >= 0.8.0)

XMLDiff\\DOM::merge — Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiff\\DOM::diff

### Опис

```methodsynopsis
public XMLDiff\DOM::merge(DOMDocument $src, DOMDocument $diff): DOMDocument
```

Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiff\\DOM::diff.

### Список параметрів

`src`

Вихідний об'єкт DOMDocument.

`diff`

Об'єкт DOMDocument, що містить інформацію, отриману за допомогою XMLDiff\\DOM::diff.

### Значення, що повертаються

Об'єднаний DOMDocument чи NULL.
