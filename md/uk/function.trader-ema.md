---
navigation:
  - function.trader-dx.md: « traderдкс
  - function.trader-errno.md: tradererrno »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderema
---
# traderema

(PECL trader >= 0.2.0)

traderema - Експоненційна ковзна середня

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
