---
navigation:
  - simplexmlelement.tostring.md: '« SimpleXMLElement::\_\_function toString() { [native code] }'
  - simplexmlelement.xpath.md: 'SimpleXMLElement::xpath »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::valid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::valid

(No version information available, might only be in Git)

SimpleXMLElement::valid — Перевіряє, чи поточний елемент є коректним.

### Опис

```methodsynopsis
public SimpleXMLElement::valid(): bool
```

**Увага**

До версії PHP 8.0 метод **SimpleXMLElement::valid()** був оголошений лише для дочірнього класу [SimpleXMLIterator](class.simplexmliterator.md)

Метод перевіряє, чи поточний елемент є коректним після викликів [SimpleXMLElement::rewind()](simplexmlelement.rewind.md) або [SimpleXMLElement::next()](simplexmlelement.next.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо поточний елемент є коректним, інакше повертає **`false`**

### Приклади

**Приклад #1 Перевірка, чи поточний елемент є коректним**

```php
<?php
$xmlElement = new SimpleXMLElement('<books><book>SQL Basics</book></books>');

$xmlElement->rewind(); // перемотка к первому элементу
echo var_dump($xmlElement->valid()); // bool(true)

$xmlElement->next(); // переход к следующему элементу
echo var_dump($xmlElement->valid()); // bool(false) поскольку существует только один элемент
?>
```
