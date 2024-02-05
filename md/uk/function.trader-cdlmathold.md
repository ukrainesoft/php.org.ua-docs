---
navigation:
  - function.trader-cdlmatchinglow.md: « trader\_cdlmatchinglow
  - function.trader-cdlmorningdojistar.md: trader\_cdlmorningdojistar »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlmathold
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlmathold

(PECL trader >= 0.2.0)

trader\_cdlmathold — Фігура Підстилка

### Опис

```methodsynopsis
trader_cdlmathold(    array $open,    array $high,    array $low,    array $close,    float $penetration = ?): array
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
