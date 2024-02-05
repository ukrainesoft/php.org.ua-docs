---
navigation:
  - function.trader-mama.md: « trader\_mama
  - function.trader-max.md: trader\_max »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_mavp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_mavp

(PECL trader >= 0.2.0)

trader\_mavp — Ковзна середня зі змінним періодом

### Опис

```methodsynopsis
trader_mavp(    array $real,    array $periods,    int $minPeriod = ?,    int $maxPeriod = ?,    int $mAType = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`periods`

Масив, що містить реальні значення.

`minPeriod`

Значення менше мінімуму буде змінено на мінімальний період. Допустимі значення від 2 до 100000

`maxPeriod`

Значення більше максимуму буде змінено на максимальний період. Допустимі значення від 2 до 100000

`mAType`

Тип ковзної середньої. Слід використовувати серію констант [TRADER\_MA\_TYPE\_\*](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
