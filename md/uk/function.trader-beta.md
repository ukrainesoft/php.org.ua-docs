---
navigation:
  - function.trader-bbands.md: « trader\_bbands
  - function.trader-bop.md: trader\_bop »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_beta
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_beta

(PECL trader >= 0.2.0)

trader\_beta — Бета

### Опис

```methodsynopsis
trader_beta(array $real0, array $real1, int $timePeriod = ?): array
```

### Список параметрів

`real0`

Масив, що містить реальні значення.

`real1`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
