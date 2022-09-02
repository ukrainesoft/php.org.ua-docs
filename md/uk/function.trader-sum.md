---
navigation:
  - function.trader-sub.md: « tradersub
  - function.trader-t3.md: tradert3 »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradersum
---
# tradersum

(PECL trader >= 0.2.0)

tradersum — Підсумовування

### Опис

```methodsynopsis
trader_sum(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
