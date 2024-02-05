---
navigation:
  - function.hexdec.md: « hexdec
  - function.intdiv.md: intdiv »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: hypot
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hypot

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

hypot - Розраховує довжину гіпотенузи прямокутного трикутника

### Опис

```methodsynopsis
hypot(float $x, float $y): float
```

Функция**hypot()** повертає довжину гіпотенузи прямокутного трикутника з довжинами сторін `x`и`y` або відстань точки (`x` `y`) до початку координат Еквівалентно виклику `sqrt($x * $x + $y * $y)`

### Список параметрів

`x`

Довжина першої сторони.

`y`

Довжина другої сторони.

### Значення, що повертаються

Повертає обчислену довжину гіпотенузи.
