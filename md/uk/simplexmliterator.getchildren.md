Повертає вкладені елементи поточного елемента

-   [« SimpleXMLIterator::current](simplexmliterator.current.md)
    
-   [SimpleXMLIterator::hasChildren »](simplexmliterator.haschildren.md)
    
-   [PHP Manual](index.md)
    
-   [SimpleXMLIterator](class.simplexmliterator.md)
    
-   Повертає вкладені елементи поточного елемента
    

# SimpleXMLIterator::getChildren

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::getChildren — Повертає вкладені елементи поточного елемента

### Опис

```methodsynopsis
public SimpleXMLIterator::getChildren(): SimpleXMLIterator
```

Цей метод повертає об'єкт [SimpleXMLIterator](class.simplexmliterator.md), що містить вкладені елементи поточного елемента [SimpleXMLIterator](class.simplexmliterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [SimpleXMLIterator](class.simplexmliterator.md)містить вкладені елементи поточного елемента.

### Приклади

**Приклад #1 Повертає вкладені елементи поточного елемента**

```php
<?php
$xml = <<<XML
<books>
    <book>
        <title>Основы PHP</title>
        <author>Джим Смит</author>
    </book>
    <book>Основы XML</book>
</books>
XML;

$xmlIterator = new SimpleXMLIterator($xml);
for( $xmlIterator->rewind(); $xmlIterator->valid(); $xmlIterator->next() ) {
    foreach($xmlIterator->getChildren() as $name => $data) {
    echo "$name: '$data' из класса " . get_class($data) . "\n";
    }
}
?>
```

Результат виконання цього прикладу:

```
title: 'Основы PHP' из класса SimpleXMLIterator
author: 'Джим Смит' из класса SimpleXMLIterator
```