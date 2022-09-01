---
navigation:
  - function.trader-obv.html: « traderobv
  - function.trader-plus-dm.html: traderplusdm »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
title: traderplusді
---
# traderplusді

(PECL trader >= 0.2.0)

traderplusdi — Плюс-спрямований індикатор

### Опис

```methodsynopsis
trader_plus_di(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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
