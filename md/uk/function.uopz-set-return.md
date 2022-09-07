---
navigation:
  - function.uopz-set-property.md: « uopzsetproperty
  - function.uopz-set-static.md: uopzsetstatic »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzsetreturn
---
# uopzsetreturn

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzsetreturn — Надати значення, що повертається для існуючої функції

### Опис

```methodsynopsis
uopz_set_return(string $function, mixed $value, bool $execute = false): bool
```

```methodsynopsis
uopz_set_return(    string $class,    string $function,    mixed $value,    bool $execute = false): bool
```

Встановити значення, що повертається для `function` на `value`. Якщо `value` замикання та встановлений `execute`, замикання буде виконуватися замість вихідної функції. Можна викликати вихідну функцію із замикання.

> **Зауваження**
> 
> Ця функція замінює [uopzrename()](function.uopz-rename.md)

### Список параметрів

`class`

Ім'я класу, що містить функцію

`function`

Ім'я існуючої функції

`value`

Значення, що повертається функцією. Якщо передано замикання та параметр execute встановлено, замикання буде виконано замість вихідної функції.

`execute`

Якщо true і у параметрі value передано замикання, замикання буде виконано замість вихідної функції.

### Значення, що повертаються

True у разі успішного виконання, false у противному випадку.

### Приклади

**Приклад #1 Приклад використання **uopzsetreturn()****

```php
<?php
uopz_set_return("strlen", 42);
echo strlen("Banana");
?>
```

Результат виконання цього прикладу:

```
42
```

**Приклад #2 Приклад використання **uopzsetreturn()****

```php
<?php
uopz_set_return("strlen", function($str) { return strlen($str) * 2; }, true );
echo strlen("Banana");
?>
```

Результат виконання цього прикладу:

```
12
```

**Приклад #3 Приклад використання **uopzsetreturn()** з класом**

```php
<?php
class My {
    public static function strlen($arg) {
        return strlen($arg);
    }
}
uopz_set_return(My::class, "strlen", function($str) { return strlen($str) * 2; }, true );
echo My::strlen("Banana");
?>
```

Результат виконання цього прикладу:

```
12
```
