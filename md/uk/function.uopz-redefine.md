---
navigation:
  - function.uopz-overload.md: « uopz\_overload
  - function.uopz-rename.md: uopz\_rename »
  - index.md: PHP Manual
  - ref.uopz.md: Функції Uopz
title: uopz\_redefine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uopz\_redefine

(PECL uopz 1, PECL uopz 2, PECL uopz 5, PECL uopz 6, PECL uopz 7)

uopz\_redefine — Перевизначити константу

### Опис

```methodsynopsis
uopz_redefine(string $constant, mixed $value): bool
```

```methodsynopsis
uopz_redefine(string $class, string $constant, mixed $value): bool
```

Переопределяет заданную константу`constant`на значение`value`

### Список параметрів

`class`

Ім'я класу, що містить константу

`constant`

Ім'я константи

`value`

Нове значення константи має бути коректним типом для постійної змінної

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** uopz\_redefine()\*\*\*\*

```php
<?php
define("MY", 100);

uopz_redefine("MY", 1000);

echo MY;
?>
```

Результат виконання наведеного прикладу:

```
1000
```
