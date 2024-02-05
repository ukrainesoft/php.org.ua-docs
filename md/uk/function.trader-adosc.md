---
navigation:
  - function.trader-add.md: « trader\_add
  - function.trader-adx.md: trader\_adx »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_adosc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_adosc

(PECL trader >= 0.2.0)

trader\_adosc - Осцилятор Чайкіна

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
