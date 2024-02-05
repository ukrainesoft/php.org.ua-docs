---
navigation:
  - function.trader-dx.md: « trader\_dx
  - function.trader-errno.md: trader\_errno »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_ema
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_ema

(PECL trader >= 0.2.0)

trader\_ema - Експоненційна ковзна середня

### Опис

```methodsynopsis
trader_ema(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
