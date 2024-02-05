---
navigation:
  - function.acosh.md: « acosh
  - function.asinh.md: asinh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: asin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# asin

(PHP 4, PHP 5, PHP 7, PHP 8)

asin - Обчислює арксинус

### Опис

```methodsynopsis
asin(float $num): float
```

Повертає арксинус числа `num`в радианах. Функция**asin()** - зворотна тригонометрична функція до функції [sin()](function.sin.md), тобто `$num == sin(asin($num))` для кожного значення параметра `num`, що входить у область значень функції **asin()**

### Список параметрів

`num`

Аргумент для обчислення

### Значення, що повертаються

Повертає арксинус числа `num` у радіанах.

### Дивіться також

-   [sin()](function.sin.md) \- обчислює синус
-   [asinh()](function.asinh.md) \- обчислює гіперболічний арксинус
-   [acos()](function.acos.md) \- обчислює арккосинус
-   [atan()](function.atan.md) \- обчислює арктангенс
