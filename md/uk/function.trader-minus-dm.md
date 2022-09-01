---
navigation:
  - function.trader-minus-di.html: « traderminusді
  - function.trader-mom.html: tradermom »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
title: traderminusдм
---
# traderminusдм

(PECL trader >= 0.2.0)

traderminusdm - Мінус-спрямований рух

### Опис

```methodsynopsis
trader_minus_dm(array $high, array $low, int $timePeriod = ?): array
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
