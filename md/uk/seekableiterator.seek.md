Переміщається до позиції

-   [« SeekableIterator](class.seekableiterator.html)
    
-   [Исключения »](spl.exceptions.html)
    
-   [PHP Manual](index.html)
    
-   [SeekableIterator](class.seekableiterator.html)
    
-   Переміщається до позиції
    

# SeekableIterator::seek

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SeekableIterator::seek — Переміщується до позиції

### Опис

```methodsynopsis
public SeekableIterator::seek(int $offset): void
```

Переміщається до заданої позиції в ітераторі.

### Список параметрів

`offset`

Позиція, до якої слід переміститися.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Реалізації мають викидати виняток [OutOfBoundsException](class.outofboundsexception.html), якщо `offset` недійсна.

### Приклади

**Приклад #1 Приклад використання **SeekableIterator::seek()****

Переміщення до елемента на 3-й позиції в ітераторі ([ArrayIterator](class.arrayiterator.html) реалізує [SeekableIterator](class.seekableiterator.html)

```php
<?php
$array = array("яблоко", "банан", "вишня", "чернослив", "ягода бузины");
$iterator = new ArrayIterator($array);
$iterator->seek(3);
echo $iterator->current();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
чернослив
```

### Дивіться також

-   [SeekableIterator](class.seekableiterator.html)
-   [Iterator](class.iterator.html)