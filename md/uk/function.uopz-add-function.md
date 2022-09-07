---
navigation:
  - ref.uopz.md: « Функції Uopz
  - function.uopz-allow-exit.md: uopzallowexit »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzaddfunction
---
# uopzaddfunction

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzaddfunction — Додає неіснуючу функцію або метод

### Опис

```methodsynopsis
uopz_add_function(string $function, Closure $handler, int &$flags = ZEND_ACC_PUBLIC): bool
```

```methodsynopsis
uopz_add_function(    string $class,    string $function,    Closure $handler,    int &$flags = ZEND_ACC_PUBLIC,    int &$all = true): bool
```

Додає неіснуючу функцію чи метод.

### Список параметрів

`class`

Назва класу.

`function`

Ім'я функції чи методу.

`handler`

Об'єкт [Closure](class.closure.md)що визначає нову функцію або метод.

`flags`

Прапори для встановлення нової функції чи методу.

`all`

Чи торкнуться всі класи, які походять від класу (`class`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**uopzaddfunction()** викидає [RuntimeException](class.runtimeexception.md), якщо функція, що додається, або метод вже існує.

### Приклади

**Приклад #1 Просте використання **uopzaddfunction()****

```php
<?php
uopz_add_function('foo', function () {echo 'bar';});
foo();
?>
```

Результат виконання цього прикладу:

```
bar
```

### Дивіться також

-   [uopzdelfunction()](function.uopz-del-function.md) - Видаляє раніше додану функцію або метод
-   [uopzsetreturn()](function.uopz-set-return.md) - Надати значення, що повертається для існуючої функції
