---
navigation:
  - function.trader-cdlmarubozu.html: « tradercdlmarubozu
  - function.trader-cdlmathold.html: tradercdlmathold »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlmatchinglow
---
# tradercdlmatchinglow

(PECL trader >= 0.2.0)

tradercdlmatchinglow - Свічкова модель "Збіг за нижнім рівнем"

### Опис

```methodsynopsis
trader_cdlmatchinglow(    array $open,    array $high,    array $low,    array $close): array
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
