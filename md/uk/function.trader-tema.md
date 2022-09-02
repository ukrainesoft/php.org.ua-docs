---
navigation:
  - function.trader-tanh.md: « tradertanh
  - function.trader-trange.md: tradertrange »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradertema
---
# tradertema

(PECL trader >= 0.2.0)

tradertema — Потрійна експоненційна ковзна середня

### Опис

```methodsynopsis
trader_tema(array $real, int $timePeriod = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
