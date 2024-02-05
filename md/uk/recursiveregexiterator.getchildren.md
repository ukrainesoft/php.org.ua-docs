---
navigation:
  - recursiveregexiterator.construct.md: '« RecursiveRegexIterator::\_\_construct'
  - recursiveregexiterator.haschildren.md: 'RecursiveRegexIterator::hasChildren »'
  - index.md: PHP Manual
  - class.recursiveregexiterator.md: RecursiveRegexIterator
title: 'RecursiveRegexIterator::getChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveRegexIterator::getChildren

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

RecursiveRegexIterator::getChildren — Повертає ітератор до поточного елемента

### Опис

```methodsynopsis
public RecursiveRegexIterator::getChildren(): RecursiveRegexIterator
```

Повертає ітератор до поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ітератор для поточного елемента, якщо можлива навігація вмісту внутрішнього ітератора.

### Помилки

Якщо внутрішній ітератор вказує на елемент, який не містить дочірніх елементів, буде викинуто виняток [InvalidArgumentException](class.invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання** RecursiveRegexIterator::getChildren()\*\*\*\*

```php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $key1 => $value1) {

    if ($rRegexIterator->hasChildren()) {

        // выведем все дочерние элементы
        echo "Дочерние элементы: ";
        foreach ($rRegexIterator->getChildren() as $key => $value) {
            echo $value . " ";
        }
        echo "\n";
    } else {
        echo "Нет дочерних элементов\n";
    }

}
?>
```

Результат виконання наведеного прикладу:

```
Нет дочерних элементов
Дочерние элементы: test4 test5
```

### Дивіться також

-   [RecursiveRegexIterator::hasChildren()](recursiveregexiterator.haschildren.md) \- Визначає, чи можлива навігація за вмістом поточного елемента
