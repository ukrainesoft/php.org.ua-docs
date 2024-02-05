---
navigation:
  - directoryiterator.next.md: '« DirectoryIterator::next'
  - directoryiterator.seek.md: 'DirectoryIterator::seek »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::rewind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::rewind

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::rewind — Перемотування ітератора DirectoryIterator назад до початку

### Опис

```methodsynopsis
public DirectoryIterator::rewind(): void
```

Перемотка итератора[DirectoryIterator](class.directoryiterator.md)назад к началу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::rewind()\*\*\*\*

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));

$iterator->next();
echo $iterator->key(); //1

$iterator->rewind(); //перемотка к началу
echo $iterator->key(); //0
?>
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.md) \- Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::key()](directoryiterator.key.md) \- Повертає ключ для поточного елемента DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) \- Перехід до наступного елементу DirectoryIterator
-   [DirectoryIterator::valid()](directoryiterator.valid.md) \- Перевіряє, чи є поточна позиція DirectoryIterator коректним файлом
-   [Iterator::rewind()](iterator.rewind.md)– Повертає ітератор на перший елемент
