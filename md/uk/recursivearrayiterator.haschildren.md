Визначає, чи є поточний елемент масивом чи об'єктом

-   [« RecursiveArrayIterator::getChildren](recursivearrayiterator.getchildren.html)
    
-   [RecursiveCachingIterator »](class.recursivecachingiterator.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveArrayIterator](class.recursivearrayiterator.html)
    
-   Визначає, чи є поточний елемент масивом чи об'єктом
    

# RecursiveArrayIterator::hasChildren

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveArrayIterator::hasChildren — Визначає, чи є поточний елемент масивом чи об'єктом

### Опис

```methodsynopsis
public RecursiveArrayIterator::hasChildren(): bool
```

Визначає, чи поточний елемент є масивом (array) або об'єктом (object). Ці відомості необхідно перевіряти, перш ніж викликати метод [RecursiveArrayIterator::getChildren()](recursivearrayiterator.getchildren.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**якщо поточний елемент є масивом (array) або об'єктом (object), **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **RecursiveArrayIterator::hasChildren()****

```php
<?php
$fruits = array("a" => "lemon", "b" => "orange", array("a" => "apple", "p" => "pear"));

$iterator = new RecursiveArrayIterator($fruits);

while ($iterator->valid()) {

    // проверим, есть ли дочерние элементы
    if ($iterator->hasChildren()) {
        // выведем информацию о дочерних элементах
        foreach ($iterator->getChildren() as $key => $value) {
            echo $key . ' : ' . $value . "\n";
        }
    } else {
        echo "Дочерних элементов нет.\n";
    }

    $iterator->next();
}
?>
```

Результат виконання цього прикладу:

```
Дочерних элементов нет.
Дочерних элементов нет.
a : apple
p : pear
```

### Дивіться також

-   [RecursiveArrayIterator::getChildren()](recursivearrayiterator.getchildren.html) - Повертає ітератор для поточного елемента, якщо елемент є масивом (array) або об'єктом (object)