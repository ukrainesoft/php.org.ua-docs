Перевизначити константу

-   [« uopz\_overload](function.uopz-overload.html)
    
-   [uopz\_rename »](function.uopz-rename.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Uopz](ref.uopz.html)
    
-   Перевизначити константу
    

# uopzredefine

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzredefine — Перевизначити константу

### Опис

```methodsynopsis
uopz_redefine(string $constant, mixed $value): bool
```

```methodsynopsis
uopz_redefine(string $class, string $constant, mixed $value): bool
```

Перевизначає задану константу `constant` на значення `value`

### Список параметрів

`class`

Ім'я класу, що містить константу

`constant`

Ім'я константи

`value`

Нове значення константи має бути коректним типом для постійної змінної

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **uopzredefine()****

```php
<?php
define("MY", 100);

uopz_redefine("MY", 1000);

echo MY;
?>
```

Результат виконання цього прикладу:

```
1000
```