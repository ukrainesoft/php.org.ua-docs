---
navigation:
  - function.trader-roc.md: « traderroc
  - function.trader-rocr100.md: traderrocr100 »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderrocp
---
# traderrocp

(PECL trader >= 0.2.0)

traderrocp — Коефіцієнт зміни у відсотках: (ціна-попередня ціна)/попередня ціна

### Опис

```methodsynopsis
trader_rocp(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
