---
navigation:
  - function.trader-aroon.md: « trader\_aroon
  - function.trader-asin.md: trader\_asin »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_aroonosc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_aroonosc

(PECL trader >= 0.2.0)

trader\_aroonosc — Осцилятор індикатора Aroon

### Опис

```methodsynopsis
trader_aroonosc(array $high, array $low, int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
