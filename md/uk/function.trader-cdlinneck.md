---
navigation:
  - function.trader-cdlidentical3crows.html: « tradercdlidentical3crows
  - function.trader-cdlinvertedhammer.html: tradercdlinvertedhammer »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlinneck
---
# tradercdlinneck

(PECL trader >= 0.2.0)

tradercdlinneck - Свічкова модель "На лінії шиї"

### Опис

```methodsynopsis
trader_cdlinneck(    array $open,    array $high,    array $low,    array $close): array
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
