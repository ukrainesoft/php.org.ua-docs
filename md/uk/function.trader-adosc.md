---
navigation:
  - function.trader-add.md: « traderadd
  - function.trader-adx.md: traderadx »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderadosc
---
# traderadosc

(PECL trader >= 0.2.0)

traderadosc - Осцилятор Чайкіна

### Опис

```methodsynopsis
trader_adosc(    array $high,    array $low,    array $close,    array $volume,    int $fastPeriod = ?,    int $slowPeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`volume`

Обсяг торгів, масив реальних значень.

`fastPeriod`

Номер періоду для швидкого ковзного середнього. Допустимі значення від 2 до 100000.

`slowPeriod`

Номер періоду для повільного ковзного середнього. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
