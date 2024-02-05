---
navigation:
  - class.recursivearrayiterator.md: « RecursiveArrayIterator
  - recursivearrayiterator.haschildren.md: 'RecursiveArrayIterator::hasChildren »'
  - index.md: PHP Manual
  - class.recursivearrayiterator.md: RecursiveArrayIterator
title: 'RecursiveArrayIterator::getChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveArrayIterator::getChildren

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

RecursiveArrayIterator::getChildren - Повертає ітератор для поточного елемента, якщо цей елемент є масивом (array) або об'єктом (object)

### Опис

```methodsynopsis
public RecursiveArrayIterator::getChildren(): ?RecursiveArrayIterator
```

Повертає ітератор до поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ітератор для поточного елемента, якщо елемент є масивом (array) чи об'єктом (object); Повертає \*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Метод викидає виняток [InvalidArgumentException](class.invalidargumentexception.md)якщо поточний елемент не містить масивів (array) або об'єктів (object).

### Приклади

**Пример #1 Пример использования**RecursiveArrayIterator::getChildren()\*\*\*\*

```php
<?php
$fruits = array("a" => "lemon", "b" => "orange", array("a" => "apple", "p" => "pear"));

$iterator = new RecursiveArrayIterator($fruits);

while ($iterator->valid()) {

    if ($iterator->hasChildren()) {
        // выводим информацию о всех дочерних элементах
        foreach ($iterator->getChildren() as $key => $value) {
            echo $key . ' : ' . $value . "\n";
        }
    } else {
        echo "Дочерних элементов не обнаружено.\n";
    }

    $iterator->next();
}
?>
```

Результат виконання наведеного прикладу:

```
Дочерних элементов не обнаружено.
Дочерних элементов не обнаружено.
a : apple
p : pear
```

### Дивіться також

-   [RecursiveArrayIterator::hasChildren()](recursivearrayiterator.haschildren.md) \- Визначає, чи є поточний елемент масивом чи об'єктом
