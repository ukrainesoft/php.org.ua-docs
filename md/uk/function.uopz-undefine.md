Скасовує визначення константи

-   [« uopzsetstatic](function.uopz-set-static.html)
    
-   [uopzunsethook »](function.uopz-unset-hook.html)
    
-   [PHP Manual](index.md)
    
-   [Функції Uopz](ref.uopz.md)
    
-   Скасовує визначення константи
    

# uopzundefine

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopzundefine — Скасує визначення константи

### Опис

```methodsynopsis
uopz_undefine(string $constant): bool
```

```methodsynopsis
uopz_undefine(string $class, string $constant): bool
```

Видаляє константу під час виконання

### Список параметрів

`class`

Назва класу, що містить `constant`

`constant`

Ім'я існуючої константи

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **uopzundefine()****

```php
<?php
define("MY", true);

uopz_undefine("MY");

var_dump(defined("MY"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
```