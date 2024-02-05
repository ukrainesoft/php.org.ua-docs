---
navigation:
  - function.uopz-set-static.md: « uopz\_set\_static
  - function.uopz-unset-hook.md: uopz\_unset\_hook »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_undefine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_undefine

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_undefine — Скасує визначення константи

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

Название класса, содержащего`constant`

`constant`

Ім'я існуючої константи

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** uopz\_undefine()\*\*\*\*

```php
<?php
define("MY", true);

uopz_undefine("MY");

var_dump(defined("MY"));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
```
