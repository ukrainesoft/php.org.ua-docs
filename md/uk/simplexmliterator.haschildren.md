Перевіряє, чи поточний елемент має вкладені елементи

-   [« SimpleXMLIterator::getChildren](simplexmliterator.getchildren.md)
    
-   [SimpleXMLIterator::key »](simplexmliterator.key.md)
    
-   [PHP Manual](index.md)
    
-   [SimpleXMLIterator](class.simplexmliterator.md)
    
-   Перевіряє, чи поточний елемент має вкладені елементи
    

# SimpleXMLIterator::hasChildren

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::hasChildren — Перевіряє, чи поточний елемент має вкладені елементи

### Опис

```methodsynopsis
public SimpleXMLIterator::hasChildren(): bool
```

Цей метод перевіряє, чи має поточний елемент [SimpleXMLIterator](class.simplexmliterator.md) вкладені елементи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

\*\*`true`\*\*якщо у поточного елемента є вкладені елементи; в іншому випадку **`false`**

### Приклади

**Приклад #1 Перевіряє, чи поточний елемент має вкладені елементи**

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

$xmlIterator = new SimpleXMLIterator( $xml );
for( $xmlIterator->rewind(); $xmlIterator->valid(); $xmlIterator->next() ) {
    if($xmlIterator->hasChildren()) {
        var_dump($xmlIterator->current());
    }
}
?>
```

Результат виконання цього прикладу:

```
object(SimpleXMLIterator)#2 (2) {
  ["title"]=>
  string(10) "Основы PHP"
  ["author"]=>
  string(9) "Джим Смит"
}
```