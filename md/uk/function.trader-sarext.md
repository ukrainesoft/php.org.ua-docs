---
navigation:
  - function.trader-sar.md: « trader\_sar
  - function.trader-set-compat.md: trader\_set\_compat »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_sarext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_sarext

(PECL trader >= 0.2.0)

trader\_sarext - Параболічний SAR - розширений

### Опис

```methodsynopsis
trader_sarext(    array $high,    array $low,    float $startValue = ?,    float $offsetOnReverse = ?,    float $accelerationInitLong = ?,    float $accelerationLong = ?,    float $accelerationMaxLong = ?,    float $accelerationInitShort = ?,    float $accelerationShort = ?,    float $accelerationMaxShort = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`startValue`

Початкове значення та напрямок. 0 для автоматичного спрямування, > 0 для довгого спрямування, < 0 для короткого спрямування. Допустимий діапазон від [TRADER\_REAL\_MIN](trader.constants.md#constant.trader-real-min)до[TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`offsetOnReverse`

Процентне зміщення додано/видалено до початкової зупинки при короткому/довгому розвороті. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`accelerationInitLong`

Початкове значення коефіцієнта прискорення для довгого спрямування. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`accelerationLong`

Коефіцієнт прискорення для довгого спрямування. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`accelerationMaxLong`

Максимальне значення коефіцієнта прискорення для довгого спрямування. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`accelerationInitShort`

Початкове значення коефіцієнта прискорення для короткого спрямування. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`accelerationShort`

Коефіцієнт прискорення для короткого спрямування. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

`accelerationMaxShort`

Максимальне значення коефіцієнта прискорення для короткого спрямування. Допустимий діапазон від 0 до [TRADER\_REAL\_MAX](trader.constants.md#constant.trader-real-max)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.
