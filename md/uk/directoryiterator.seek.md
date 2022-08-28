Переміщує покажчик DirectoryIterator на певну позицію

-   [« DirectoryIterator::rewind](directoryiterator.rewind.html)
    
-   [DirectoryIterator::\_\_toString »](directoryiterator.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Переміщує покажчик DirectoryIterator на певну позицію
    

# DirectoryIterator::seek

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DirectoryIterator::seek — Переміщує покажчик DirectoryIterator на певну позицію

### Опис

```methodsynopsis
public DirectoryIterator::seek(int $offset): void
```

Переміщує покажчик [DirectoryIterator](class.directoryiterator.html) на певну позицію.

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

-   [DirectoryIterator::rewind()](directoryiterator.rewind.html) - Встановлює покажчик на перший елемент DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.html) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [SeekableIterator::seek()](seekableiterator.seek.html) - Переміщається до позиції