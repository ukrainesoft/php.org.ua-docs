---
navigation:
  - function.trader-cdlmorningdojistar.md: « trader\_cdlmorningdojistar
  - function.trader-cdlonneck.md: trader\_cdlonneck »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlmorningstar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlmorningstar

(PECL trader >= 0.2.0)

trader\_cdlmorningstar - Ранкова зірка

### Опис

```methodsynopsis
trader_cdlmorningstar(    array $open,    array $high,    array $low,    array $close,    float $penetration = ?): array
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

`penetration`

Відсоток проникнення однієї свічки всередині іншої свічки.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
