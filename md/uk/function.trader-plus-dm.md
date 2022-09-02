---
navigation:
  - function.trader-plus-di.md: « traderplusді
  - function.trader-ppo.md: traderppo »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderplusдм
---
# traderplusдм

(PECL trader >= 0.2.0)

traderplusdm - Плюс-спрямований рух

### Опис

```methodsynopsis
trader_plus_dm(array $high, array $low, int $timePeriod = ?): array
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
