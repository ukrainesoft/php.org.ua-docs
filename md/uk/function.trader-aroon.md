---
navigation:
  - function.trader-apo.md: « traderapo
  - function.trader-aroonosc.md: traderaroonosc »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderaroon
---
# traderaroon

(PECL trader >= 0.2.0)

traderaroon — Індикатор Aroon

### Опис

```methodsynopsis
trader_aroon(array $high, array $low, int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
