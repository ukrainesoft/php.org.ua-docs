---
navigation:
  - function.strrchr.md: « strrchr
  - function.strripos.md: strripos »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: стр'їв
---
# стр'їв

(PHP 4, PHP 5, PHP 7, PHP 8)

strrev — Перевертає рядок задом наперед

### Опис

```methodsynopsis
strrev(string $string): string
```

Повертає рядок `string`, перевернутою задом наперед.

### Список параметрів

`string`

Перевертається рядок.

### Значення, що повертаються

Повертає перевернутий рядок.

### Приклади

**Приклад #1 Приклад використання **стр'єв()****

```php
<?php
echo strrev("Hello world!"); // выводит "!dlrow olleH"
?>
```
