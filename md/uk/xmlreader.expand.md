---
navigation:
  - xmlreader.close.html: '« XMLReader::close'
  - xmlreader.getattribute.html: 'XMLReader::getAttribute »'
  - index.html: PHP Manual
  - class.xmlreader.html: XMLReader
title: 'XMLReader::expand'
---
# XMLReader::expand

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::expand — Повернути копію поточного сайту як об'єкт DOM

### Опис

```methodsynopsis
public XMLReader::expand(?DOMNode $baseNode = null): DOMNode|false
```

Цей метод копіює поточний вузол та повертає відповідний об'єкт DOM.

### Список параметрів

`baseNode`

[DOMNode](class.domnode.html) визначає цільовий [DOMDocument](class.domdocument.html) створеного об'єкта DOM.

### Значення, що повертаються

Результатуючий [DOMNode](class.domnode.html) або **`false`** у разі виникнення помилки.
