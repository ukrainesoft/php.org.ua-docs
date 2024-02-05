---
navigation:
  - function.uopz-flags.md: « uopz\_flags
  - function.uopz-get-exit-status.md: uopz\_get\_exit\_status »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_function

(PECL uopz 1, PECL uopz 2)

uopz\_function — Створює функцію під час виконання

**Увага**

Ця функція була *ВИДАЛЕНО*в PECL uopz 5.0.0.

### Опис

```methodsynopsis
uopz_function(string $function, Closure $handler, int $modifiers = ?): void
```

```methodsynopsis
uopz_function(    string $class,    string $function,    Closure $handler,    int $modifiers = ?): void
```

Створює функцію під час виконання

### Список параметрів

`class`

Ім'я класу для отримання нової функції

`function`

Ім'я функції

`handler`

Замикання для функції

`modifiers`

Модифікатори для функції, скопійовані за замовчуванням або ZEND\_ACC\_PUBLIC

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** uopz\_function()\*\*\*\*

```php
<?php
uopz_function("my_strlen", function($arg) {
    return strlen($arg);
});
echo my_strlen("Привет, Мир");
?>
```

Результат виконання наведеного прикладу:

```
11
```

**Приклад #2 Приклад використання** uopz\_function()\*\* з класом\*\*

```php
<?php
class My {}

uopz_function(My::class, "strlen", function($arg) {
    return strlen($arg);
}, ZEND_ACC_STATIC);

echo My::strlen("Привет, Мир");
?>
```

Результат виконання наведеного прикладу:

```
11
```
