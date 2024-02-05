---
navigation:
  - simplexmlelement.getnamespaces.md: '« SimpleXMLElement::getNamespaces'
  - simplexmlelement.haschildren.md: 'SimpleXMLElement::hasChildren »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::getChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::getChildren

(No version information available, might only be in Git)

SimpleXMLElement::getChildren — Повертає дочірні елементи поточного елемента

### Опис

```methodsynopsis
public SimpleXMLElement::getChildren(): ?SimpleXMLElement
```

**Увага**

До версії PHP 8.0 метод **SimpleXMLElement::getChildren()** був оголошений лише для дочірнього класу [SimpleXMLIterator](class.simplexmliterator.md)

Метод повертає об'єкт [SimpleXMLElement](class.simplexmlelement.md), що містить дочірні елементи поточного елемента [SimpleXMLElement](class.simplexmlelement.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [SimpleXMLElement](class.simplexmlelement.md)містить дочірні елементи поточного елемента.

### Приклади

**Приклад #1 Повернення дочірніх елементів поточного елемента**

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
    foreach($xmlElement->getChildren() as $name => $data) {
        echo "Значением $name является '$data' из класса " . get_class($data) . "\n";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
Значением title является 'PHP Basics' из класса SimpleXMLElement
Значением author является 'Jim Smith' из класса SimpleXMLElement
```
