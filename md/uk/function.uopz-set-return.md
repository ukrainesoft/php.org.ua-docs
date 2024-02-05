---
navigation:
  - function.uopz-set-property.md: « uopz\_set\_property
  - function.uopz-set-static.md: uopz\_set\_static »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_set\_return
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_set\_return

(PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_set\_return — Надати значення, що повертається для існуючої функції

### Опис

```methodsynopsis
uopz_set_return(string $function, mixed $value, bool $execute = false): bool
```

```methodsynopsis
uopz_set_return(    string $class,    string $function,    mixed $value,    bool $execute = false): bool
```

Установить возвращаемое значение для`function`на`value`. Якщо `value` замикання та встановлений `execute`, замикання буде виконуватися замість вихідної функції. Можна викликати вихідну функцію із замикання.

> **Зауваження** :
> 
> Ця функція замінює [uopz\_rename()](function.uopz-rename.md)

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

**Пример #1 Пример использования**uopz\_set\_return()\*\*\*\*

```php
<?php
uopz_set_return("strlen", 42);
echo strlen("Banana");
?>
```

Результат виконання наведеного прикладу:

```
42
```

**Пример #2 Пример использования**uopz\_set\_return()\*\*\*\*

```php
<?php
uopz_set_return("strlen", function($str) { return strlen($str) * 2; }, true );
echo strlen("Banana");
?>
```

Результат виконання наведеного прикладу:

```
12
```

**Пример #3 Пример использования**uopz\_set\_return()\*\* з класом\*\*

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

Результат виконання наведеного прикладу:

```
12
```
