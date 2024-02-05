---
navigation:
  - arrayiterator.offsetset.md: '« ArrayIterator::offsetSet'
  - arrayiterator.rewind.md: 'ArrayIterator::rewind »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::offsetUnset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayIterator::offsetUnset

(PHP 5, PHP 7, PHP 8)

ArrayIterator::offsetUnset — Скидає значення зі зміщення

### Опис

```methodsynopsis
public ArrayIterator::offsetUnset(mixed $key): void
```

Скидає значення зі зміщення.

Якщо ітерація виконується та **ArrayIterator::offsetUnset()** використовується для скидання поточного індексу ітерації, позиція ітерації буде зміщена до наступного індексу. Оскільки позиція ітерації також зміщується наприкінці [foreach](control-structures.foreach.md)в теле цикла, использование\*\*ArrayIterator::offsetUnset()\*\*внутри цикла[`foreach`](control-structures.foreach.md) може призвести до пропуску індексів.

### Список параметрів

`key`

Зміщення для скидання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ArrayIterator::offsetGet()](arrayiterator.offsetget.md) \- Отримує значення для усунення
-   [ArrayIterator::offsetSet()](arrayiterator.offsetset.md) \- Встановлює значення для усунення
