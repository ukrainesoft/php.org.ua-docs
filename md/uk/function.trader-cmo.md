---
navigation:
  - function.trader-ceil.md: « trader\_ceil
  - function.trader-correl.md: trader\_correl »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cmo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cmo

(PECL trader >= 0.2.0)

trader\_cmo — Осцилятор цінових моментів Чанде

### Опис

```methodsynopsis
trader_cmo(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
