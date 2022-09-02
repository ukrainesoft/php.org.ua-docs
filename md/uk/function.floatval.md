---
navigation:
  - function.empty.md: « empty
  - function.get-debug-type.md: getdebugtype »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: floatval
---
# floatval

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

floatval — Повертає значення змінної у вигляді числа з точкою, що плаває

### Опис

```methodsynopsis
floatval(mixed $value): float
```

Повертає значення змінної `value` у вигляді числа з плаваючою точкою (float).

### Список параметрів

`value`

Можливо будь-якого скалярного типу . **floatval()** не можна використовувати з об'єктами, у цьому випадку виникне помилка рівня **`E_NOTICE`** та функція поверне 1.

### Значення, що повертаються

Значення заданої змінної як числа з плаваючою точкою. Порожні масиви як аргумент повертають 0, непусті масиви повертають 1.

Рядки найчастіше повертають 0, проте результат залежить від найлівіших символів рядка. Застосовуються правила [приведения к float](language.types.float.md#language.types.float.casting)

### Приклади

**Приклад #1 Приклад використання **floatval()****

```php
<?php
$var = '122.34343The';
$float_value_of_var = floatval($var);
echo $float_value_of_var; // 122.34343
?>
```

**Приклад #2 Приклад використання **floatval()** з нечисловими крайніми лівими символами**

```php
<?php
$var = 'The122.34343';
$float_value_of_var = floatval($var);
echo $float_value_of_var; // 0
?>
```

### Дивіться також

-   [boolval()](function.boolval.md) - Повертає логічне значення змінної
-   [intval()](function.intval.md) - Повертає ціле значення змінної
-   [strval()](function.strval.md) - Повертає строкове значення змінної
-   [settype()](function.settype.md) - Задає тип змінної
-   [Маніпуляції з типами](language.types.type-juggling.md)
