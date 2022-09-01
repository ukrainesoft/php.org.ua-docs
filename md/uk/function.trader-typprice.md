---
navigation:
  - function.trader-tsf.html: « tradertsf
  - function.trader-ultosc.html: traderultosc »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradertypprice
---
# tradertypprice

(PECL trader >= 0.2.0)

tradertypprice — Типова ціна

### Опис

```methodsynopsis
trader_typprice(array $high, array $low, array $close): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
