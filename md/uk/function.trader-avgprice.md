---
navigation:
  - function.trader-atr.md: « traderatr
  - function.trader-bbands.md: traderbbands »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderavgprice
---
# traderavgprice

(PECL trader >= 0.2.0)

traderavgprice — Середня ціна

### Опис

```methodsynopsis
trader_avgprice(    array $open,    array $high,    array $low,    array $close): array
```

### Список параметрів

`open`

Ціна відкриття масив реальних значень.

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
