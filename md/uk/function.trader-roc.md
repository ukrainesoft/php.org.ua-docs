---
navigation:
  - function.trader-ppo.md: « traderppo
  - function.trader-rocp.md: traderrocp »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderroc
---
# traderroc

(PECL trader >= 0.2.0)

traderroc — Швидкість зміни: ((ціна/попередня ціна)-1)

### Опис

```methodsynopsis
trader_roc(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
