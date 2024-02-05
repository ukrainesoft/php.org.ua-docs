---
navigation:
  - function.sin.md: « sin
  - function.sqrt.md: sqrt »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: sinh
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sinh

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

sinh - Обчислює гіперболічний синус

### Опис

```methodsynopsis
sinh(float $num): float
```

Повертає гіперболічний синус числа `num`, який визначено в результаті обчислення `(exp($num) - exp(-$num))/2`

### Список параметрів

`num`

Аргумент для обчислення.

### Значення, що повертаються

Повертає гіперболічний синус числа `num`

### Дивіться також

-   [sin()](function.sin.md) \- обчислює синус
-   [asinh()](function.asinh.md) \- обчислює гіперболічний арксинус
-   [cosh()](function.cosh.md) \- обчислює гіперболічний косинус
-   [tanh()](function.tanh.md) \- обчислює гіперболічний тангенс
