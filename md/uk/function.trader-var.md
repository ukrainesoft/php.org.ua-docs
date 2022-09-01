---
navigation:
  - function.trader-ultosc.html: « traderultosc
  - function.trader-wclprice.html: traderwclprice »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
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
