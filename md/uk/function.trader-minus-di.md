---
navigation:
  - function.trader-minmaxindex.md: « traderminmaxindex
  - function.trader-minus-dm.md: traderminusdm »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderminusді
---
# traderminusді

(PECL trader >= 0.2.0)

traderminusdi - Мінус-спрямований індикатор

### Опис

```methodsynopsis
trader_minus_di(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
