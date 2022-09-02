---
navigation:
  - function.trader-ultosc.md: « traderultosc
  - function.trader-wclprice.md: traderwclprice »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradervar
---
# tradervar

(PECL trader >= 0.2.0)

tradervar - Варіація

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
