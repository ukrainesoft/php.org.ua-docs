---
navigation:
  - function.abs.md: « abs
  - function.acosh.md: acosh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: acos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# acos

(PHP 4, PHP 5, PHP 7, PHP 8)

acos - Обчислює арккосинус

### Опис

```methodsynopsis
acos(float $num): float
```

Возвращает арккосинус аргумента`num`в радианах. Функция**acos()** - зворотна тригонометрична функція до функції [cos()](function.cos.md), тобто `$num == cos(acos($num))` для кожного значення параметра `num`, що входить у область значень функції **acos()**

### Список параметрів

`num`

Аргумент для обчислення

### Значення, що повертаються

Повертає арккосинус числа `num` у радіанах.

### Дивіться також

-   [cos()](function.cos.md) \- обчислює косинус
-   [acosh()](function.acosh.md) \- обчислює гіперболічний арккосинус
-   [asin()](function.asin.md) \- обчислює арксинус
-   [atan()](function.atan.md) \- обчислює арктангенс
