---
navigation:
  - function.trader-minmaxindex.md: « trader\_minmaxindex
  - function.trader-minus-dm.md: trader\_minus\_dm »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_minus\_di
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_minus\_di

(PECL trader >= 0.2.0)

trader\_minus\_di - Мінус-спрямований індикатор

### Опис

```methodsynopsis
trader_minus_di(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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
