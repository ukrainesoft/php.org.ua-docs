---
navigation:
  - function.trader-rocr100.md: « traderrocr100
  - function.trader-rsi.md: traderrsi »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderrocr
---
# traderrocr

(PECL trader >= 0.2.0)

traderrocr — Коефіцієнт зміни курсу: (ціна/попередня ціна)

### Опис

```methodsynopsis
trader_rocr(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
