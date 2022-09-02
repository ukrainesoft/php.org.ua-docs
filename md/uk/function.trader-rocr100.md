---
navigation:
  - function.trader-rocp.md: « traderrocp
  - function.trader-rocr.md: traderrocr »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderrocr100
---
# traderrocr100

(PECL trader >= 0.2.0)

traderrocr100 — Коефіцієнт зміни курсу шкали: (ціна/попередня ціна)

### Опис

```methodsynopsis
trader_rocr100(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
