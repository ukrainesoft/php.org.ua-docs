---
navigation:
  - function.atan2.md: « atan2
  - function.atanh.md: atanh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: atan
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# atan

(PHP 4, PHP 5, PHP 7, PHP 8)

atan - Обчислює арктангенс

### Опис

```methodsynopsis
atan(float $num): float
```

Возвращает арктангенс числа`num`в радианах. Функция**atan()** - зворотна тригонометрична функція до функції [tan()](function.tan.md), тобто `$num == tan(atan($num))` для кожного значення числа `num`, що входить у область значень функції **atan()**

### Список параметрів

`num`

Аргумент для обчислення

### Значення, що повертаються

Возвращает арктангенс числа`num` у радіанах.

### Дивіться також

-   [tan()](function.tan.md) \- обчислює тангенс
-   [atanh()](function.atanh.md) \- обчислює гіперболічний арктангенс
-   [asin()](function.asin.md) \- обчислює арксинус
-   [acos()](function.acos.md) \- обчислює арккосинус
