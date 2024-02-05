---
navigation:
  - directoryiterator.isdot.md: '« DirectoryIterator::isDot'
  - directoryiterator.next.md: 'DirectoryIterator::next »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::key'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::key

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::key — Повертає ключ для поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::key(): mixed
```

Повертає ключ для поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ для поточного елемента [DirectoryIterator](class.directoryiterator.md) як цілого числа (int).

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | При помилці ініціалізації ітератора тепер видається помилка [Error](class.error.md); раніше метод повертав значення **`false`** |

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::key()\*\*\*\*

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if (!$fileinfo->isDot()) {
        echo $fileinfo->key() . " => " . $fileinfo->getFilename() . "\n";
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
0 => apple.jpg
1 => banana.jpg
2 => index.php
3 => pear.jpg
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.md) \- Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) \- Перехід до наступного елементу DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) \- Перемотування ітератора DirectoryIterator назад до початку
-   [DirectoryIterator::valid()](directoryiterator.valid.md) \- Перевіряє, чи є поточна позиція DirectoryIterator коректним файлом
-   [Iterator::key()](iterator.key.md) \- Повертає ключ поточного елемента
