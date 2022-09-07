---
navigation:
  - xmldiff-dom.diff.md: '« XMLDiffDOM::diff'
  - class.xmldiff-memory.md: XMLDiffMemory »
  - index.md: PHP Manual
  - class.xmldiff-dom.md: XMLDiffDOM
title: 'XMLDiffDOM::merge'
---
# XMLDiffDOM::merge

(PECL xmldiff >= 0.8.0)

XMLDiffDOM::merge — Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff

### Опис

```methodsynopsis
public XMLDiff\DOM::merge(DOMDocument $src, DOMDocument $diff): DOMDocument
```

Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff.

### Список параметрів

`src`

Вихідний об'єкт DOMDocument.

`diff`

Об'єкт DOMDocument, що містить інформацію, отриману за допомогою XMLDiffDOM::diff.

### Значення, що повертаються

Об'єднаний DOMDocument чи NULL.
