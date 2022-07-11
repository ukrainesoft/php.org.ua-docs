- [ trader_sar](function.trader-sar.md)
- [trader_set_compat »](function.trader-set-compat.md)

- [PHP Manual](index.md)
- [Функції Trader](ref.trader.md)
- Параболічний SAR – розширений

# trader_sarext

(PECL trader \>= 0.2.0)

trader_sarext - Параболічний SAR - розширений

### Опис

**trader_sarext**(
array `$high`,
array `$low`,
float `$startValue` = ?,
float `$offsetOnReverse` = ?,
float `$accelerationInitLong` = ?,
float `$accelerationLong` = ?,
float `$accelerationMaxLong` = ?,
float `$accelerationInitShort` = ?,
float `$accelerationShort` = ?,
float `$accelerationMaxShort` = ?
): array

### Список параметрів

`high`
Висока вартість, масив реальних значень.

`low`
Низька вартість, масив реальних значень.

`startValue`
Початкове значення та напрямок. 0 для автоматичного спрямування, \>
0 для довгого напрямку, \<0 для короткого напрямку. Допустимий
діапазон від
[TRADER_REAL_MIN](trader.constants.md#constant.trader-real-min) до
[TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

`offsetOnReverse`
Відсоткове зміщення додано/видалено до початкової зупинки при
короткому/довгому розвороті. Допустимий діапазон від 0 до
[TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

`accelerationInitLong`
Початкове значення коефіцієнта прискорення для довгого спрямування.
Допустимий діапазон від 0 до
[TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

`accelerationLong`
Коефіцієнт прискорення для довгого спрямування. Допустимий діапазон від 0
до [TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

`accelerationMaxLong`
Максимальне значення коефіцієнта прискорення для довгого спрямування.
Допустимий діапазон від 0 до
[TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

`accelerationInitShort`
Початкове значення коефіцієнта прискорення для короткого спрямування.
Допустимий діапазон від 0 до
[TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

`accelerationShort`
Коефіцієнт прискорення для короткого спрямування. Допустимий діапазон від
0 до [TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

`accelerationMaxShort`
Максимальне значення коефіцієнта прискорення для короткого спрямування.
Допустимий діапазон від 0 до
[TRADER_REAL_MAX](trader.constants.md#constant.trader-real-max).

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі
виникнення помилки.
