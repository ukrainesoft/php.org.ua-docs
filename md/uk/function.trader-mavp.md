---
navigation:
  - function.trader-mama.md: « tradermama
  - function.trader-max.md: tradermax »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradermavp
---
# tradermavp

(PECL trader >= 0.2.0)

tradermavp — Ковзна середня зі змінним періодом

### Опис

```methodsynopsis
trader_mavp(    array $real,    array $periods,    int $minPeriod = ?,    int $maxPeriod = ?,    int $mAType = ?): array
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

Тип ковзної середньої. Слід використовувати серію констант [TRADERМАTYPE](trader.constants.md)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
