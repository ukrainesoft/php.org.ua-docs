---
navigation:
  - class.seekableiterator.md: « SeekableIterator
  - spl.exceptions.md: Винятки »
  - index.md: PHP Manual
  - class.seekableiterator.md: SeekableIterator
title: 'SeekableIterator::seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SeekableIterator::seek

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

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

Реалізації мають викидати виняток [OutOfBoundsException](class.outofboundsexception.md), якщо `offset` недійсна.

### Приклади

**Приклад #1 Приклад використання** SeekableIterator::seek()\*\*\*\*

Переміщення до елемента на 3-й позиції в ітераторі ([ArrayIterator](class.arrayiterator.md) реалізує [SeekableIterator](class.seekableiterator.md)

```php
<?php
$array = array("яблоко", "банан", "вишня", "чернослив", "ягода бузины");
$iterator = new ArrayIterator($array);
$iterator->seek(3);
echo $iterator->current();
?>
```

Висновок наведеного прикладу буде схожим на:

```
чернослив
```

### Дивіться також

-   [SeekableIterator](class.seekableiterator.md)
-   [Iterator](class.iterator.md)
