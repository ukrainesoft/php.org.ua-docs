---
navigation:
  - function.trader-cdlengulfing.md: « trader\_cdlengulfing
  - function.trader-cdleveningstar.md: trader\_cdleveningstar »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdleveningdojistar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdleveningdojistar

(PECL trader >= 0.2.0)

trader\_cdleveningdojistar — Вечірня дожі-зірка

### Опис

```methodsynopsis
trader_cdleveningdojistar(    array $open,    array $high,    array $low,    array $close,    float $penetration = ?): array
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
