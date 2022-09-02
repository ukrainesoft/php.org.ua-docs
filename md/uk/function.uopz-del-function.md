---
navigation:
  - function.uopz-copy.md: « uopzcopy
  - function.uopz-delete.md: uopzdelete »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzdelfunction
---
# uopzdelfunction

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzdelfunction — Видалення раніше доданої функції або методу

### Опис

```methodsynopsis
uopz_del_function(string $function): bool
```

```methodsynopsis
uopz_del_function(string $class, string $function, int &$all = true): bool
```

Видалення раніше доданої функції або методу.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

`all`

Чи торкнуться всі класи, які походять від класу (`class`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**uopzdelfunction()** викидає [RuntimeException](class.runtimeexception.md), якщо видалені функції або метод не були додані за допомогою [uopzaddfunction()](function.uopz-add-function.md)

### Приклади

**Приклад #1 Просте використання **uopzdelfunction()****

```php
<?php
uopz_add_function('foo', function () {echo 'bar';});
var_dump(function_exists('foo'));
uopz_del_function('foo');
var_dump(function_exists('foo'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [uopzaddfunction()](function.uopz-add-function.md) - Додає неіснуючу функцію чи метод
-   [uopzunsetreturn()](function.uopz-unset-return.md) - Скасує раніше встановлене значення, що повертається для функції
