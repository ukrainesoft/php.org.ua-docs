Визначає, чи можлива навігація за вмістом поточного елемента

-   [« RecursiveRegexIterator::getChildren](recursiveregexiterator.getchildren.html)
    
-   [RecursiveTreeIterator »](class.recursivetreeiterator.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveRegexIterator](class.recursiveregexiterator.html)
    
-   Визначає, чи можлива навігація за вмістом поточного елемента
    

# RecursiveRegexIterator::hasChildren

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RecursiveRegexIterator::hasChildren — Визначає, чи можлива навігація за вмістом поточного елемента

### Опис

```methodsynopsis
public RecursiveRegexIterator::hasChildren(): bool
```

Визначає, чи можлива навігація вмісту поточного елемента. Якщо поточний елемент має дочірні елементи, ітератор для них можна отримати методом [RecursiveRegexIterator::getChildren()](recursiveregexiterator.getchildren.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо можлива навігація вмісту поточного елемента, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **RecursiveRegexIterator::hasChildren()****

```php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $value) {
    var_dump($rRegexIterator->hasChildren());
}
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [RecursiveRegexIterator::getChildren()](recursiveregexiterator.getchildren.html) - Повертає ітератор для поточного елемента