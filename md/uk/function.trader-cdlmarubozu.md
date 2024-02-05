---
navigation:
  - function.trader-cdllongline.md: « trader\_cdllongline
  - function.trader-cdlmatchinglow.md: trader\_cdlmatchinglow »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlmarubozu
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlmarubozu

(PECL trader >= 0.2.0)

trader\_cdlmarubozu — Марубозу.

### Опис

```methodsynopsis
trader_cdlmarubozu(    array $open,    array $high,    array $low,    array $close): array
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
