---
navigation:
  - domelement.getattribute.md: '« DOMElement::getAttribute'
  - domelement.getattributenode.md: 'DOMElement::getAttributeNode »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::getAttributeNames'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::getAttributeNames

(PHP 8 >= 8.3.0)

DOMElement::getAttributeNames — Отримує імена атрибутів

### Опис

```methodsynopsis
public DOMElement::getAttributeNames(): array
```

Отримує імена атрибутів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод повертає імена атрибутів.

### Приклади

**Приклад #1 Приклад использования метода**DOMElement::getAttributeNames()\*\*\*\*

```php
<?php

$dom = new DOMDocument();
$dom->loadXML('<html xmlns:some="some:ns" some:test="a" test2="b"/>');
var_dump($dom->documentElement->getAttributeNames());
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
 [0]=>
 string(10) "xmlns:some"
 [1]=>
 string(9) "some:test"
 [2]=>
 string(5) "test2"
}
```
