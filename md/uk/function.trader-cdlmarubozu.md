---
navigation:
  - function.trader-cdllongline.md: « tradercdllongline
  - function.trader-cdlmatchinglow.md: tradercdlmatchinglow »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlmarubozu
---
# tradercdlmarubozu

(PECL trader >= 0.2.0)

tradercdlmarubozu — Марубозу.

### Опис

```methodsynopsis
trader_cdlmarubozu(    array $open,    array $high,    array $low,    array $close): array
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
