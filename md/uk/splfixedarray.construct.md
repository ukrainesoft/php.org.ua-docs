---
navigation:
  - class.splfixedarray.md: « SplFixedArray
  - splfixedarray.count.md: 'SplFixedArray::count »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::construct'
---
# SplFixedArray::construct

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplFixedArray::construct - Створює новий масив фіксованої довжини

### Опис

public **SplFixedArray::construct**(int `$size`

Створює фіксований масив із числом **`null`** значень, рівних `size`

### Список параметрів

`size`

Розмір фіксованого масиву. Очікується значення між `0` і **`PHP_INT_MAX`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `size` від'ємний.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `size` від'ємний; раніше викидався виняток [InvalidArgumentException](class.invalidargumentexception.md) |

### Приклади

**Приклад #1 Приклад використання **SplFixedArray::construct()****

```php
<?php
$array = new SplFixedArray(5);

$array[1] = 2;
$array[4] = "foo";

foreach($array as $v) {
  var_dump($v);
}
?>
```

Результат виконання цього прикладу:

```
NULL
int(2)
NULL
NULL
string(3) "foo"
```
