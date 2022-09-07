---
navigation:
  - function.trader-sum.md: « tradersum
  - function.trader-tan.md: tradertan »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderтз
---
# traderтз

(PECL trader >= 0.2.0)

tradert3 - Потрійна експоненційна ковзна середня

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
