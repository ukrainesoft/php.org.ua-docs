Повертає поточний елемент

-   [« SimpleXMLIterator](class.simplexmliterator.html)
    
-   [SimpleXMLIterator::getChildren »](simplexmliterator.getchildren.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXMLIterator](class.simplexmliterator.html)
    
-   Повертає поточний елемент
    

# SimpleXMLIterator::current

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::current — Повертає поточний елемент

### Опис

```methodsynopsis
public SimpleXMLIterator::current(): mixed
```

Цей метод повертає поточний елемент як об'єкт класу [SimpleXMLIterator](class.simplexmliterator.html) або **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний елемент як об'єкт класу [SimpleXMLIterator](class.simplexmliterator.html) або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Повернення поточного елемента**

```php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>Основы PHP</book><book>Основы XML</book></books>');
var_dump($xmlIterator->current());

$xmlIterator->rewind(); // сбрасывает курсор к первому элементу
var_dump($xmlIterator->current());
?>
```

Результат виконання цього прикладу:

```
NULL
object(SimpleXMLIterator)#2 (1) {
  [0]=>
  string(10) "Основы PHP"
}
```

### Дивіться також

-   [SimpleXMLIterator::key()](simplexmliterator.key.html) - Повертає поточний ключ
-   [SimpleXMLIterator::next()](simplexmliterator.next.html) - Переміщує ітератор до наступного елементу
-   [SimpleXMLIterator::rewind()](simplexmliterator.rewind.html) - Повертає ітератор до першого елементу
-   [SimpleXMLIterator::valid()](simplexmliterator.valid.html) - Перевіряє, чи є поточний елемент допустимим
-   [SimpleXMLElement](class.simplexmlelement.html)