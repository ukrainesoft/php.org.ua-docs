---
navigation:
  - function.trader-cosh.html: « tradercosh
  - function.trader-div.html: traderdiv »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderdema
---
# traderdema

(PECL trader >= 0.2.0)

traderdema — Подвійна експоненційна ковзна середня

### Опис

```methodsynopsis
trader_dema(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
