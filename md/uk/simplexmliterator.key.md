Повертає поточний ключ

-   [« SimpleXMLIterator::hasChildren](simplexmliterator.haschildren.html)
    
-   [SimpleXMLIterator::next »](simplexmliterator.next.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXMLIterator](class.simplexmliterator.html)
    
-   Повертає поточний ключ
    

# SimpleXMLIterator::key

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::key — Повертає поточний ключ

### Опис

```methodsynopsis
public SimpleXMLIterator::key(): mixed
```

Цей метод отримує ім'я тега XML поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я XML-тегу елемента, на який посилається поточний об'єкт [SimpleXMLIterator](class.simplexmliterator.html), або **`false`**

### Приклади

**Приклад #1 Отримує ім'я поточного тега XML**

```php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>Основы PHP</book><book>Основы XML</book></books>');

echo var_dump($xmlIterator->key());
$xmlIterator->rewind(); // возврат к первому элементу
echo var_dump($xmlIterator->key());

?>
```

Результат виконання цього прикладу:

```
bool(false)
string(4) "book"
```