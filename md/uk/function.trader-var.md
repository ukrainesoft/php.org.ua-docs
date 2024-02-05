---
navigation:
  - function.trader-ultosc.md: « trader\_ultosc
  - function.trader-wclprice.md: trader\_wclprice »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_var
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_var

(PECL trader >= 0.2.0)

trader\_var - Варіація

### Опис

```methodsynopsis
trader_var(array $real, int $timePeriod = ?, float $nbDev = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`nbDev`

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
