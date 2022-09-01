---
navigation:
  - function.trader-rocr.html: « traderrocr
  - function.trader-sar.html: tradersar »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderrsi
---
# traderrsi

(PECL trader >= 0.2.0)

traderrsi - Індекс відносної сили

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
