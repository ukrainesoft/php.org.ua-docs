---
navigation:
  - function.trader-ht-trendmode.md: « trader\_ht\_trendmode
  - function.trader-linearreg-angle.md: trader\_linearreg\_angle »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_kama
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_kama

(PECL trader >= 0.2.0)

trader\_kama - Адаптивна ковзна середня Кауфмана

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
