---
navigation:
  - function.trader-minus-di.md: « trader\_minus\_di
  - function.trader-mom.md: trader\_mom »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_minus\_dm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_minus\_dm

(PECL trader >= 0.2.0)

trader\_minus\_dm - Мінус-спрямований рух

### Опис

```methodsynopsis
trader_minus_dm(array $high, array $low, int $timePeriod = ?): array
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
