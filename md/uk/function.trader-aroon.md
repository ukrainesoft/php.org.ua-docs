---
navigation:
  - function.trader-apo.md: « trader\_apo
  - function.trader-aroonosc.md: trader\_aroonosc »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_aroon
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_aroon

(PECL trader >= 0.2.0)

trader\_aroon - Індикатор Aroon

### Опис

```methodsynopsis
trader_aroon(array $high, array $low, int $timePeriod = ?): array
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
