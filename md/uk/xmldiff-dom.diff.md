---
navigation:
  - class.xmldiff-dom.html: « XMLDiffDOM
  - xmldiff-dom.merge.html: 'XMLDiffDOM::merge »'
  - index.html: PHP Manual
  - class.xmldiff-dom.html: XMLDiffDOM
title: 'XMLDiffDOM::diff'
---
# XMLDiffDOM::diff

(PECL xmldiff >= 0.8.0)

XMLDiffDOM::diff — Пошук відмінностей у двох об'єктах DOMDocument

### Опис

```methodsynopsis
public XMLDiff\DOM::diff(DOMDocument $from, DOMDocument $to): DOMDocument
```

Шукає відмінності у двох об'єктах DOMDocument та повертає новий об'єкт, що містить ці відмінності.

### Список параметрів

`from`

Вихідний об'єкт DOMDocument.

`to`

Об'єкт DOMDocument, з яким проводиться порівняння.

### Значення, що повертаються

Новий об'єкт DOMDocument з інформацією про знайдені відмінності, або NULL.
