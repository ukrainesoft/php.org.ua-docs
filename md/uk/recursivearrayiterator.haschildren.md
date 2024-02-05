---
navigation:
  - recursivearrayiterator.getchildren.md: '« RecursiveArrayIterator::getChildren'
  - class.recursivecachingiterator.md: RecursiveCachingIterator »
  - index.md: PHP Manual
  - class.recursivearrayiterator.md: RecursiveArrayIterator
title: 'RecursiveArrayIterator::hasChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveArrayIterator::hasChildren

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

RecursiveArrayIterator::hasChildren — Визначає, чи є поточний елемент масивом чи об'єктом

### Опис

```methodsynopsis
public RecursiveArrayIterator::hasChildren(): bool
```

Визначає, чи поточний елемент є масивом (array) або об'єктом (object). Ці відомості необхідно перевіряти, перш ніж викликати метод [RecursiveArrayIterator::getChildren()](recursivearrayiterator.getchildren.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо поточний елемент є масивом (array) або об'єктом (object), **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**RecursiveArrayIterator::hasChildren()\*\*\*\*

```php
<?php
$fruits = array("a" => "lemon", "b" => "orange", array("a" => "apple", "p" => "pear"));

$iterator = new RecursiveArrayIterator($fruits);

while ($iterator->valid()) {

    // проверим, есть ли дочерние элементы
    if ($iterator->hasChildren()) {
        // выведем информацию о дочерних элементах
        foreach ($iterator->getChildren() as $key => $value) {
            echo $key . ' : ' . $value . "\n";
        }
    } else {
        echo "Дочерних элементов нет.\n";
    }

    $iterator->next();
}
?>
```

Результат виконання наведеного прикладу:

```
Дочерних элементов нет.
Дочерних элементов нет.
a : apple
p : pear
```

### Дивіться також

-   [RecursiveArrayIterator::getChildren()](recursivearrayiterator.getchildren.md) \- Повертає ітератор для поточного елемента, якщо елемент є масивом (array) або об'єктом (object)
