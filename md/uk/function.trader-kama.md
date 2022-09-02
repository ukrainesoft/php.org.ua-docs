---
navigation:
  - function.trader-ht-trendmode.md: « traderхтtrendmode
  - function.trader-linearreg-angle.md: traderlinearregangle »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderkama
---
# traderkama

(PECL trader >= 0.2.0)

traderkama - Адаптивна ковзна середня Кауфмана

### Опис

```methodsynopsis
trader_kama(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
