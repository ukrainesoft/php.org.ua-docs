---
navigation:
  - function.log10.md: « log10
  - function.log.md: log »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: log1p
---
# log1p

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

log1p - Повертає log(1 + number), розрахований так, що результат точний, навіть якщо значення number близько до нуля

### Опис

```methodsynopsis
log1p(float $num): float
```

**log1p()** повертає log(1 + `num`), розраховане таким чином, що результат точний, навіть коли значення `num` близько до нуля. Через нестачу точності [log()](function.log.md) у разі може повернути просто log(1).

### Список параметрів

`num`

Вхідне значення

### Значення, що повертаються

log(1 + `num`

### Дивіться також

-   [expm1()](function.expm1.md) - Повертає exp(number) - 1, розраховане таким чином, що результат точний навіть якщо значення number близько до нуля.
-   [log()](function.log.md) - Натуральний логарифм
-   [log10()](function.log10.md) - Десятковий логарифм
