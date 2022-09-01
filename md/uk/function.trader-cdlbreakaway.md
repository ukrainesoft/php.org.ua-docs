---
navigation:
  - function.trader-cdlbelthold.html: « tradercdlbelthold
  - function.trader-cdlclosingmarubozu.html: tradercdlclosingmarubozu »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlbreakaway
---
# tradercdlbreakaway

(PECL trader >= 0.2.0)

tradercdlbreakaway - Відрив

### Опис

```methodsynopsis
trader_cdlbreakaway(    array $open,    array $high,    array $low,    array $close): array
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
