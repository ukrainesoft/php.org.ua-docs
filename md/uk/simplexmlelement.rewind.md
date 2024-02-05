---
navigation:
  - simplexmlelement.registerxpathnamespace.md: '« SimpleXMLElement::registerXPathNamespace'
  - simplexmlelement.savexml.md: 'SimpleXMLElement::saveXML »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::rewind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::rewind

(No version information available, might only be in Git)

SimpleXMLElement::rewind — Перемотування до першого елементу

### Опис

```methodsynopsis
public SimpleXMLElement::rewind(): void
```

**Увага**

До версії PHP 8.0 метод **SimpleXMLElement::rewind()** був оголошений лише для дочірнього класу [SimpleXMLIterator](class.simplexmliterator.md)

Метод перемотує [SimpleXMLElement](class.simplexmlelement.md) до першого елементу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Перемотування до першого елемента**

```php
<?php
$xmlElement = new SimpleXMLElement('<books><book>PHP Basics</book><book>XML Basics</book></books>');
$xmlElement->rewind();

var_dump($xmlElement->current());
?>
```

Результат виконання наведеного прикладу:

```
object(SimpleXMLElement)#2 (1) {
  [0]=>
  string(10) "PHP Basics"
}
```
