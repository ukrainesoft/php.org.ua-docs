---
navigation:
  - function.trader-cdlmarubozu.md: « trader\_cdlmarubozu
  - function.trader-cdlmathold.md: trader\_cdlmathold »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlmatchinglow
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlmatchinglow

(PECL trader >= 0.2.0)

trader\_cdlmatchinglow - Свічкова модель "Збіг за нижнім рівнем"

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
