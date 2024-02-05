---
navigation:
  - function.strrchr.md: « strrchr
  - function.strripos.md: strripos »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strrev
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strrev

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

**Приклад #1 Приклад використання** strrev()\*\*\*\*

```php
<?php
echo strrev("Hello world!"); // выводит "!dlrow olleH"
?>
```
