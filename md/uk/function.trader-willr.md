---
navigation:
  - function.trader-wclprice.md: « traderwclprice
  - function.trader-wma.md: traderwma »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderwillr
---
# traderwillr

(PECL trader >= 0.2.0)

traderwillr - Відсотковий діапазон Вільямса

### Опис

```methodsynopsis
trader_willr(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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
