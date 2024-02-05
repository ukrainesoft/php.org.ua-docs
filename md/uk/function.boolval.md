---
navigation:
  - ref.var.md: « Функції для роботи зі змінними
  - function.debug-zval-dump.md: debug\_zval\_dump »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: boolval
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# boolval

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

boolval - Повертає логічне значення змінної

### Опис

```methodsynopsis
boolval(mixed $value): bool
```

Повертає логічне значення (bool) параметра `value`

### Список параметрів

`value`

Скалярне значення, яке слід привести до типу bool.

### Значення, що повертаються

Повертає наведене до логічного типу (bool) значення параметра `value`

### Приклади

**Приклад #1 Приклад використання** boolval()\*\*\*\*

```php
<?php
echo '0:        '.(boolval(0) ? 'true' : 'false')."\n";
echo '42:       '.(boolval(42) ? 'true' : 'false')."\n";
echo '0.0:      '.(boolval(0.0) ? 'true' : 'false')."\n";
echo '4.2:      '.(boolval(4.2) ? 'true' : 'false')."\n";
echo '"":       '.(boolval("") ? 'true' : 'false')."\n";
echo '"string": '.(boolval("string") ? 'true' : 'false')."\n";
echo '"0":      '.(boolval("0") ? 'true' : 'false')."\n";
echo '"1":      '.(boolval("1") ? 'true' : 'false')."\n";
echo '[1, 2]:   '.(boolval([1, 2]) ? 'true' : 'false')."\n";
echo '[]:       '.(boolval([]) ? 'true' : 'false')."\n";
echo 'stdClass: '.(boolval(new stdClass) ? 'true' : 'false')."\n";
?>
```

Результат виконання наведеного прикладу:

```
0:        false
42:       true
0.0:      false
4.2:      true
"":       false
"string": true
"0":      false
"1":      true
[1, 2]:   true
[]:       false
stdClass: true
```

### Дивіться також

-   [floatval()](function.floatval.md) \- Повертає значення змінної у вигляді числа з плаваючою точкою
-   [intval()](function.intval.md) \- Повертає ціле значення змінної
-   [strval()](function.strval.md) \- Повертає строкове значення змінної
-   [settype()](function.settype.md) \- Задає тип змінної
-   [is\_bool()](function.is-bool.md) \- Перевіряє, чи є змінна логічне значення
-   [Перетворення типів](language.types.type-juggling.md)
