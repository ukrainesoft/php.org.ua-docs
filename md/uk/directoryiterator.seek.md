---
navigation:
  - directoryiterator.rewind.md: '« DirectoryIterator::rewind'
  - directoryiterator.tostring.md: 'DirectoryIterator::\_\_toString »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::seek

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DirectoryIterator::seek — Перехід до елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::seek(int $offset): void
```

Перехід до заданої позиції [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

`offset`

Числова позиція, що починається з нуля, до якої потрібно перейти.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::seek()\*\*\*\*

Перехід до четвертого елементу каталогу, що містить скрипт. Першими двома зазвичай є и `.. .`

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
$iterator->seek(3);
if ($iterator->valid()) {
    echo $iterator->getFilename();
} else {
    echo 'Отсутствие файла в позиции 3';
}
?>
```

### Дивіться також

-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) \- Перемотування ітератора DirectoryIterator назад до початку
-   [DirectoryIterator::next()](directoryiterator.next.md) \- Перехід до наступного елементу DirectoryIterator
-   [SeekableIterator::seek()](seekableiterator.seek.md) \- переміщається до позиції
