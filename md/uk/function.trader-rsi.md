---
navigation:
  - function.trader-rocr.md: « trader\_rocr
  - function.trader-sar.md: trader\_sar »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_rsi
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_rsi

(PECL trader >= 0.2.0)

trader\_rsi - Індекс відносної сили

### Опис

```methodsynopsis
trader_rsi(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
