---
navigation:
  - function.trader-sub.md: « trader\_sub
  - function.trader-t3.md: trader\_t3 »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_sum
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_sum

(PECL trader >= 0.2.0)

trader\_sum — Підсумовування

### Опис

```methodsynopsis
trader_sum(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
