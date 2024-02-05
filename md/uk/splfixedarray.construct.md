---
navigation:
  - class.splfixedarray.md: « SplFixedArray
  - splfixedarray.count.md: 'SplFixedArray::count »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplFixedArray::\_\_construct - Створює новий масив фіксованої довжини

### Опис

public**SplFixedArray::\_\_construct**(int`$size`

Створює фіксований масив із числом **`null`** значень, рівних `size`

### Список параметрів

`size`

Розмір фіксованого масиву. Очікується значення між и\*\*`PHP_INT_MAX`\*\*

### Помилки

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `size`отрицателен.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `size` від'ємний; раніше викидався виняток [InvalidArgumentException](class.invalidargumentexception.md) |

### Приклади

**Пример #1 Пример использования**SplFixedArray::\_\_construct()\*\*\*\*

```php
<?php
$array = new SplFixedArray(5);

$array[1] = 2;
$array[4] = "foo";

foreach($array as $v) {
  var_dump($v);
}
?>
```

Результат виконання наведеного прикладу:

```
NULL
int(2)
NULL
NULL
string(3) "foo"
```
