---
navigation:
  - function.trader-cdlstalledpattern.md: « tradercdlstalledpattern
  - function.trader-cdltakuri.md: tradercdltakuri »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlsticksandwich
---
# tradercdlsticksandwich

(PECL trader >= 0.2.0)

tradercdlsticksandwich - Прилиплий сендвіч

### Опис

```methodsynopsis
trader_cdlsticksandwich(    array $open,    array $high,    array $low,    array $close): array
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
