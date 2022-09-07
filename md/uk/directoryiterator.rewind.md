---
navigation:
  - directoryiterator.next.md: '« DirectoryIterator::next'
  - directoryiterator.seek.md: 'DirectoryIterator::seek »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::rewind'
---
# DirectoryIterator::rewind

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::rewind — Встановлює вказівник на перший елемент DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::rewind(): void
```

Встановлює вказівник на перший елемент [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::rewind()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));

$iterator->next();
echo $iterator->key(); //1

$iterator->rewind(); //переход к началу
echo $iterator->key(); //0
?>
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.md) - Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::key()](directoryiterator.key.md) - Повертає ключ поточного елемента DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [DirectoryIterator::valid()](directoryiterator.valid.md) - Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом
-   [Iterator::rewind()](iterator.rewind.md) – Повертає ітератор на перший елемент
