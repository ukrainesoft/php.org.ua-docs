---
navigation:
  - function.trader-beta.html: « traderbeta
  - function.trader-cci.html: tradercci »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderbop
---
# traderbop

(PECL trader >= 0.2.0)

traderbop - Баланс сил

### Опис

```methodsynopsis
trader_bop(    array $open,    array $high,    array $low,    array $close): array
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
