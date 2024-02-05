---
navigation:
  - ref.uopz.md: « Функції Uopz
  - function.uopz-allow-exit.md: uopz\_allow\_exit »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_add\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_add\_function

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_add\_function — Додає неіснуючу функцію або метод

### Опис

```methodsynopsis
uopz_add_function(string $function, Closure $handler, int &$flags = ZEND_ACC_PUBLIC): bool
```

```methodsynopsis
uopz_add_function(    string $class,    string $function,    Closure $handler,    int &$flags = ZEND_ACC_PUBLIC,    int &$all = true): bool
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**uopz\_add\_function()** викидає [RuntimeException](class.runtimeexception.md), якщо функція, що додається, або метод вже існує.

### Приклади

**Пример #1 Простое использование**uopz\_add\_function()\*\*\*\*

```php
<?php
uopz_add_function('foo', function () {echo 'bar';});
foo();
?>
```

Результат виконання наведеного прикладу:

```
bar
```

### Дивіться також

-   [uopz\_del\_function()](function.uopz-del-function.md) \- Видаляє раніше додану функцію або метод
-   [uopz\_set\_return()](function.uopz-set-return.md) \- Надати значення, що повертається для існуючої функції
