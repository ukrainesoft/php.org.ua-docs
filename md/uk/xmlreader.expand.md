---
navigation:
  - xmlreader.close.md: '« XMLReader::close'
  - xmlreader.getattribute.md: 'XMLReader::getAttribute »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::expand'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::expand

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::expand — Повернути копію поточного сайту як об'єкт DOM

### Опис

```methodsynopsis
public XMLReader::expand(?DOMNode $baseNode = null): DOMNode|false
```

Цей метод копіює поточний вузол та повертає відповідний об'єкт DOM.

### Список параметрів

`baseNode`

[DOMNode](class.domnode.md) визначає цільовий [DOMDocument](class.domdocument.md) створеного об'єкта DOM.

### Значення, що повертаються

Результирующий[DOMNode](class.domnode.md)или\*\*`false`\*\*в случае возникновения ошибки.
