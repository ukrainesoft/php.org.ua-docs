---
navigation:
  - splfixedarray.current.md: '« SplFixedArray::current'
  - splfixedarray.getsize.md: 'SplFixedArray::getSize »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::fromArray'
---
# SplFixedArray::fromArray

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplFixedArray::fromArray - Імпортує PHP-масив в об'єкт класу [SplFixedArray](class.splfixedarray.md)

### Опис

```methodsynopsis
public static SplFixedArray::fromArray(array $array, bool $preserveKeys = true): SplFixedArray
```

Імпортує PHP-масив `array` у новий об'єкт класу [SplFixedArray](class.splfixedarray.md)

### Список параметрів

`array`

Масив, який слід імпортувати.

`preserveKeys`

Наскільки можна зберегти чисельні індекси, задані в оригінальному масиві.

### Значення, що повертаються

Повертає об'єкт класу [SplFixedArray](class.splfixedarray.md)містить дані з імпортованого масиву.

### Приклади

**Приклад #1 Приклад використання **SplFixedArray::fromArray()****

```php
<?php
$fa = SplFixedArray::fromArray(array(1 => 1, 0 => 2, 3 => 3));

var_dump($fa);

$fa = SplFixedArray::fromArray(array(1 => 1, 0 => 2, 3 => 3), false);

var_dump($fa);
?>
```

Результат виконання цього прикладу:

```
object(SplFixedArray)#1 (4) {
  [0]=>
  int(2)
  [1]=>
  int(1)
  [2]=>
  NULL
  [3]=>
  int(3)
}
object(SplFixedArray)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
