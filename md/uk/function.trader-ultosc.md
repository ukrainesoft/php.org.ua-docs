---
navigation:
  - function.trader-typprice.md: « trader\_typprice
  - function.trader-var.md: trader\_var »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_ultosc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_ultosc

(PECL trader >= 0.2.0)

trader\_ultosc - Остаточний, граничний осцилятор

### Опис

```methodsynopsis
trader_ultosc(    array $high,    array $low,    array $close,    int $timePeriod1 = ?,    int $timePeriod2 = ?,    int $timePeriod3 = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`timePeriod1`

Кількість барів (стовпців) за 1-й період. Допустимий діапазон від 1 до 100000.

`timePeriod2`

Кількість барів (стовпців) за 2-й період. Допустимий діапазон від 1 до 100000.

`timePeriod3`

Кількість барів (стовпців) за 3-й період. Допустимий діапазон від 1 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
