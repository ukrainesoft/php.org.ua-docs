---
navigation:
  - function.trader-ppo.md: « trader\_ppo
  - function.trader-rocp.md: trader\_rocp »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_roc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_roc

(PECL trader >= 0.2.0)

trader\_roc — Швидкість зміни: ((ціна/попередня ціна)-1)\*

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
