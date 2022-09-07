---
navigation:
  - function.uopz-set-static.md: « uopzsetstatic
  - function.uopz-unset-hook.md: uopzunsethook »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopzundefine
---
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
define("MY", true);

uopz_undefine("MY");

var_dump(defined("MY"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
```
