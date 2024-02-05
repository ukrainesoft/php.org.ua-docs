---
navigation:
  - recursiveregexiterator.getchildren.md: '« RecursiveRegexIterator::getChildren'
  - class.recursivetreeiterator.md: RecursiveTreeIterator »
  - index.md: PHP Manual
  - class.recursiveregexiterator.md: RecursiveRegexIterator
title: 'RecursiveRegexIterator::hasChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveRegexIterator::hasChildren

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

RecursiveRegexIterator::hasChildren — Визначає, чи можлива навігація за вмістом поточного елемента

### Опис

```methodsynopsis
public RecursiveRegexIterator::hasChildren(): bool
```

Визначає, чи можлива навігація вмісту поточного елемента. Якщо поточний елемент має дочірні елементи, ітератор для них можна отримати методом [RecursiveRegexIterator::getChildren()](recursiveregexiterator.getchildren.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо можлива навігація вмісту поточного елемента, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** RecursiveRegexIterator::hasChildren()\*\*\*\*

```php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $value) {
    var_dump($rRegexIterator->hasChildren());
}
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [RecursiveRegexIterator::getChildren()](recursiveregexiterator.getchildren.md) \- Повертає ітератор для поточного елемента
