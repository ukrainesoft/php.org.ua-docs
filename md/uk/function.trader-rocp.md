---
navigation:
  - function.trader-roc.md: « trader\_roc
  - function.trader-rocr100.md: trader\_rocr100 »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_rocp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_rocp

(PECL trader >= 0.2.0)

trader\_rocp — Коефіцієнт зміни у відсотках: (ціна-попередня ціна)/попередня ціна

### Опис

```methodsynopsis
trader_rocp(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
