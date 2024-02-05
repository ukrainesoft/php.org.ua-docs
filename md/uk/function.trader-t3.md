---
navigation:
  - function.trader-sum.md: « trader\_sum
  - function.trader-tan.md: trader\_tan »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_t3
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_t3

(PECL trader >= 0.2.0)

trader\_t3 - Потрійна експоненційна ковзна середня

### Опис

```methodsynopsis
trader_t3(array $real, int $timePeriod = ?, float $vFactor = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

`vFactor`

Коефіцієнт обсягу. Допустимі значення від 1 до 0.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
