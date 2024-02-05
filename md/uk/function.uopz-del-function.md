---
navigation:
  - function.uopz-copy.md: « uopz\_copy
  - function.uopz-delete.md: uopz\_delete »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_del\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_del\_function

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_del\_function — Видалення раніше доданої функції або методу

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**uopz\_del\_function()** викидає [RuntimeException](class.runtimeexception.md), якщо видалені функції або метод не були додані за допомогою [uopz\_add\_function()](function.uopz-add-function.md)

### Приклади

**Пример #1 Простое использование**uopz\_del\_function()\*\*\*\*

```php
<?php
uopz_add_function('foo', function () {echo 'bar';});
var_dump(function_exists('foo'));
uopz_del_function('foo');
var_dump(function_exists('foo'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [uopz\_add\_function()](function.uopz-add-function.md) \- Додає неіснуючу функцію чи метод
-   [uopz\_unset\_return()](function.uopz-unset-return.md) \- Скасує раніше встановлене значення, що повертається для функції
