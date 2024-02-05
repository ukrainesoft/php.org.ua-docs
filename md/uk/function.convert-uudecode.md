---
navigation:
  - function.convert-cyr-string.md: « convert\_cyr\_string
  - function.convert-uuencode.md: convert\_uuencode »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: convert\_uudecode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# convert\_uudecode

(PHP 5, PHP 7, PHP 8)

convert\_uudecode — Декодує рядок із формату uuencode у звичайний вигляд

### Опис

```methodsynopsis
convert_uudecode(string $string): string|false
```

**convert\_uudecode()** декодує рядок із формату uuencode у звичайний вигляд.

> **Зауваження** **convert\_uudecode()** не приймає ні початкової (`begin`), ні кінцевої (`end`) рядки, яка є частиною файлів (*files*) uuencoded.

### Список параметрів

`string`

Дані у форматі uuencode.

### Значення, що повертаються

Повертає декодовані дані у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** convert\_uudecode()\*\*\*\*

```php
<?php
echo convert_uudecode("+22!L;W9E(%!(4\"$`\n`");
?>
```

Результат виконання наведеного прикладу:

```
I love PHP!
```

### Дивіться також

-   [convert\_uuencode()](function.convert-uuencode.md) \- Кодує рядок у форматі uuencode
