---
navigation:
  - function.trader-adx.md: « traderadx
  - function.trader-apo.md: traderapo »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderadxr
---
# traderadxr

(PECL trader >= 0.2.0)

traderadxr - Середній рейтинг індексу спрямованого руху

### Опис

```methodsynopsis
trader_adxr(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
