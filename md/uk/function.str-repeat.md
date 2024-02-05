---
navigation:
  - function.str-pad.md: « str\_pad
  - function.str-replace.md: str\_replace »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: str\_repeat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# str\_repeat

(PHP 4, PHP 5, PHP 7, PHP 8)

str\_repeat — Повертає рядок, що повторюється.

### Опис

```methodsynopsis
str_repeat(string $string, int $times): string
```

Повертає рядок `string`, повторенную`times`раз.

### Список параметрів

`string`

Повторюваний рядок.

`times`

Кількість разів, які потрібно повторити рядок `string`

`times` повинен бути більшим або дорівнює нулю. Якщо `times` дорівнює нулю, повертається порожній рядок.

### Значення, що повертаються

Повертає рядок, що повторюється.

### Приклади

**Пример #1 Пример использования**str\_repeat()\*\*\*\*

```php
<?php
echo str_repeat("-=", 10);
?>
```

Результат виконання наведеного прикладу:

```
-=-=-=-=-=-=-=-=-=-=
```

### Дивіться також

-   [for](control-structures.for.md)
-   [str\_pad()](function.str-pad.md) \- Доповнює рядок іншим рядком до заданої довжини
-   [substr\_count()](function.substr-count.md) \- Повертає кількість входжень підрядка
