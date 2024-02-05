---
navigation:
  - function.trader-atan.md: « trader\_atan
  - function.trader-avgprice.md: trader\_avgprice »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_atr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_atr

(PECL trader >= 0.2.0)

trader\_atr — Середній дійсний діапазон

### Опис

```methodsynopsis
trader_atr(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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
