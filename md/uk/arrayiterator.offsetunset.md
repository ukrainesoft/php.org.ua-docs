---
navigation:
  - arrayiterator.offsetset.html: '« ArrayIterator::offsetSet'
  - arrayiterator.rewind.html: 'ArrayIterator::rewind »'
  - index.html: PHP Manual
  - class.arrayiterator.html: ArrayIterator
title: 'ArrayIterator::offsetUnset'
---
# ArrayIterator::offsetUnset

(PHP 5, PHP 7, PHP 8)

ArrayIterator::offsetUnset — Скидає значення зі зміщення

### Опис

```methodsynopsis
public ArrayIterator::offsetUnset(mixed $key): void
```

Скидає значення зі зміщення.

Якщо ітерація виконується та **ArrayIterator::offsetUnset()** використовується для скидання поточного індексу ітерації, позиція ітерації буде зміщена до наступного індексу. Оскільки позиція ітерації також зміщується наприкінці [foreach](control-structures.foreach.html) у тілі циклу, використання **ArrayIterator::offsetUnset()** всередині циклу [`foreach`](control-structures.foreach.html) може призвести до пропуску індексів.

### Список параметрів

`key`

Зміщення для скидання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ArrayIterator::offsetGet()](arrayiterator.offsetget.html) - Отримує значення для зміщення
-   [ArrayIterator::offsetSet()](arrayiterator.offsetset.html) - Встановлює значення для усунення
