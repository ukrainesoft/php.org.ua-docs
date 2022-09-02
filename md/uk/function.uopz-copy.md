---
navigation:
  - function.uopz-compose.md: « uopzcompose
  - function.uopz-del-function.md: uopzdelfunction »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzcopy
---
# uopzcopy

(PECL uopz 1 >= 1.0.4, PECL uopz 2)

uopzcopy — Копіювати функцію

**Увага**

Ця функція була *ВИДАЛЕНО* у PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_copy(string $function): Closure
```

```methodsynopsis
uopz_copy(string $class, string $function): Closure
```

Копіювати функцію на ім'я

### Список параметрів

`class`

Ім'я класу, що містить функцію копіювання

`function`

Ім'я функції

### Значення, що повертаються

Об'єкт Closure для певної функції

### Приклади

**Приклад #1 Приклад використання **uopzcopy()****

```php
<?php
$strtotime = uopz_copy('strtotime');

uopz_function("strtotime", function($arg1, $arg2) use($strtotime) {
    /* зесь можно вызвать оригинальную функцию strtotime */
    var_dump($arg1);
});

var_dump(strtotime('dummy'));
?>
```

Результат виконання цього прикладу:

```
string(5) "dummy"
```
