---
navigation:
  - function.trader-rocp.md: « trader\_rocp
  - function.trader-rocr.md: trader\_rocr »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_rocr100
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_rocr100

(PECL trader >= 0.2.0)

trader\_rocr100 — Коефіцієнт зміни курсу шкали: (ціна/попередня ціна)\*

### Опис

```methodsynopsis
trader_rocr100(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
