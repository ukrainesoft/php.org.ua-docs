---
navigation:
  - function.uopz-unset-mock.md: « uopz\_unset\_mock
  - book.wincache.md: WinCache »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_unset\_return
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_unset\_return

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_unset\_return — Скасує раніше встановлене значення для функції

### Опис

```methodsynopsis
uopz_unset_return(string $function): bool
```

```methodsynopsis
uopz_unset_return(string $class, string $function): bool
```

Отменяет возвращаемое значение`function`, ранее заданное функцией[uopz\_set\_return()](function.uopz-set-return.md)

### Список параметрів

`class`

Ім'я класу, що містить функцію

`function`

Ім'я функції

### Значення, що повертаються

True у разі успішного виконання

### Приклади

**Приклад #1 Приклад використання** uopz\_unset\_return()\*\*\*\*

```php
<?php
uopz_set_return("strlen", 42);
$len = strlen("Banana");
uopz_unset_return("strlen");
echo $len + strlen("Banana");
?>
```

Результат виконання наведеного прикладу:

```
48
```
