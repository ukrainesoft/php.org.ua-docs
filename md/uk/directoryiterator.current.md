---
navigation:
  - directoryiterator.construct.md: '« DirectoryIterator::\_\_construct'
  - directoryiterator.getbasename.md: 'DirectoryIterator::getBasename »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::current'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::current

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::current — Повертає поточний елемент DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::current(): mixed
```

Отримує поточний елемент [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний елемент [DirectoryIterator](class.directoryiterator.md)

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::current()\*\*\*\*

У цьому прикладі буде виведено вміст каталогу, що містить скрипт.

```php
<?php
$iterator = new DirectoryIterator(__DIR__);
while($iterator->valid()) {
    $file = $iterator->current();
    echo $iterator->key() . " => " . $file->getFilename() . "\n";
    $iterator->next();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
0 => .
1 => ..
2 => apple.jpg
3 => banana.jpg
4 => index.php
5 => pear.jpg
```

### Дивіться також

-   [DirectoryIterator::key()](directoryiterator.key.md) \- Повертає ключ для поточного елемента DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) \- Перехід до наступного елементу DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) \- Перемотування ітератора DirectoryIterator назад до початку
-   [DirectoryIterator::valid()](directoryiterator.valid.md) \- Перевіряє, чи є поточна позиція DirectoryIterator коректним файлом
-   [Iterator::current()](iterator.current.md) \- Повернення поточного елемента
