---
navigation:
  - simplexmlelement.key.md: '« SimpleXMLElement::key'
  - simplexmlelement.registerxpathnamespace.md: 'SimpleXMLElement::registerXPathNamespace »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::next

(No version information available, might only be in Git)

SimpleXMLElement::next — Перехід до наступного елемента

### Опис

```methodsynopsis
public SimpleXMLElement::next(): void
```

**Увага**

До версії PHP 8.0 метод **SimpleXMLElement::next()** був оголошений лише для дочірнього класу [SimpleXMLIterator](class.simplexmliterator.md)

Метод перемещает[SimpleXMLElement](class.simplexmlelement.md) до наступного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Перейти до наступного елемента**

```php
<?php
$xmlElement = new SimpleXMLElement('<books><book>PHP Basics</book><book>XML basics</book></books>');
$xmlElement->rewind(); // перемотка к первому элементу
$xmlElement->next();

var_dump($xmlElement->current());
?>
```

Результат виконання наведеного прикладу:

```
object(SimpleXMLElement)#2 (1) {
  [0]=>
  string(10) "XML basics"
}
```
