---
navigation:
  - function.trader-cdlspinningtop.md: « trader\_cdlspinningtop
  - function.trader-cdlsticksandwich.md: trader\_cdlsticksandwich »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_cdlstalledpattern
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_cdlstalledpattern

(PECL trader >= 0.2.0)

trader\_cdlstalledpattern - Гальмування

### Опис

```methodsynopsis
trader_cdlstalledpattern(    array $open,    array $high,    array $low,    array $close): array
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
