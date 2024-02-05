---
navigation:
  - function.trader-adx.md: « trader\_adx
  - function.trader-apo.md: trader\_apo »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_adxr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_adxr

(PECL trader >= 0.2.0)

trader\_adxr - Середній рейтинг індексу спрямованого руху

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
