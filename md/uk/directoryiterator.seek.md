---
navigation:
  - directoryiterator.rewind.md: '« DirectoryIterator::rewind'
  - directoryiterator.tostring.md: 'DirectoryIterator::toString »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::seek'
---
# DirectoryIterator::seek

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DirectoryIterator::seek — Переміщує покажчик DirectoryIterator на певну позицію

### Опис

```methodsynopsis
public DirectoryIterator::seek(int $offset): void
```

Переміщує покажчик [DirectoryIterator](class.directoryiterator.md) на певну позицію.

### Список параметрів

`offset`

Номер позиції для переміщення. Нумерація починається із нуля.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::seek()****

Перейти до четвертого елемента в директорії, що містить скрипт. Перші два, як правило `.` і `..`

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
$iterator->seek(3);
if ($iterator->valid()) {
    echo $iterator->getFilename();
} else {
    echo 'Нет третьего элемента в директории';
}
?>
```

### Дивіться також

-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) - Встановлює покажчик на перший елемент DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [SeekableIterator::seek()](seekableiterator.seek.md) - Переміщається до позиції
