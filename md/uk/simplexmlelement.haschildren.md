---
navigation:
  - simplexmlelement.getchildren.md: '« SimpleXMLElement::getChildren'
  - simplexmlelement.key.md: 'SimpleXMLElement::key »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::hasChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::hasChildren

(No version information available, might only be in Git)

SimpleXMLElement::hasChildren — Перевіряє, чи поточний елемент має дочірні елементи

### Опис

```methodsynopsis
public SimpleXMLElement::hasChildren(): bool
```

**Увага**

До версії PHP 8.0 метод **SimpleXMLElement::hasChildren()** був оголошений лише для дочірнього класу [SimpleXMLIterator](class.simplexmliterator.md)

Метод перевіряє, чи має поточний елемент [SimpleXMLElement](class.simplexmlelement.md) дочірніх елементів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо поточний елемент має дочірні елементи, інакше повертає **`false`**

### Приклади

**Приклад #1 Перевірка наявності поточного елемента дочірніх елементів**

```php
<?php
$xml = <<<XML
<books>
    <book>
        <title>PHP Basics</title>
        <author>Jim Smith</author>
    </book>
    <book>XML basics</book>
</books>
XML;

$xmlElement = new SimpleXMLElement($xml);
for ($xmlElement->rewind(); $xmlElement->valid(); $xmlElement->next()) {
    if ($xmlElement->hasChildren()) {
        var_dump($xmlElement->current());
    }
}
?>
```

Результат виконання наведеного прикладу:

```
object(SimpleXMLElement)#2 (2) {
  ["title"]=>
  string(10) "PHP Basics"
  ["author"]=>
  string(9) "Jim Smith"
}
```
