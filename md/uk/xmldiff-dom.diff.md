---
navigation:
  - class.xmldiff-dom.md: « XMLDiff\\DOM
  - xmldiff-dom.merge.md: 'XMLDiff\\DOM::merge »'
  - index.md: PHP Manual
  - class.xmldiff-dom.md: XMLDiff\\DOM
title: 'XMLDiff\\DOM::diff'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLDiff\\DOM::diff

(PECL xmldiff >= 0.8.0)

XMLDiff\\DOM::diff — Пошук відмінностей у двох об'єктах DOMDocument

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
