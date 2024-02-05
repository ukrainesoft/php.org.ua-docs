---
navigation:
  - directoryiterator.key.md: '« DirectoryIterator::key'
  - directoryiterator.rewind.md: 'DirectoryIterator::rewind »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::next

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::next — Перехід до наступного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::next(): void
```

Перехід до наступного елементу [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**DirectoryIterator::next()\*\*\*\*

Перерахуйте вміст каталогу за допомогою циклу while.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
while($iterator->valid()) {
    echo $iterator->getFilename() . "\n";
    $iterator->next();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
.
..
apple.jpg
banana.jpg
index.php
pear.jpg
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.md) \- Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::key()](directoryiterator.key.md) \- Повертає ключ для поточного елемента DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) \- Перемотування ітератора DirectoryIterator назад до початку
-   [DirectoryIterator::valid()](directoryiterator.valid.md) \- Перевіряє, чи є поточна позиція DirectoryIterator коректним файлом
-   [Iterator::next()](iterator.next.md) \- Переходить до наступного елементу
