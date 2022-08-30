Параболічний SAR – розширений

-   [« tradersar](function.trader-sar.html)
    
-   [tradersetcompat »](function.trader-set-compat.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Параболічний SAR – розширений
    

# tradersarext

(PECL trader >= 0.2.0)

tradersarext - Параболічний SAR - розширений

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

Початкове значення та напрямок. 0 для автоматичного спрямування, > 0 для довгого спрямування, < 0 для короткого спрямування. Допустимий діапазон від [TRADERREALMIN](trader.constants.html#constant.trader-real-min) до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

`offsetOnReverse`

Процентне зміщення додано/видалено до початкової зупинки при короткому/довгому розвороті. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

`accelerationInitLong`

Початкове значення коефіцієнта прискорення для довгого спрямування. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

`accelerationLong`

Коефіцієнт прискорення для довгого спрямування. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

`accelerationMaxLong`

Максимальне значення коефіцієнта прискорення для довгого спрямування. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

`accelerationInitShort`

Початкове значення коефіцієнта прискорення для короткого спрямування. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

`accelerationShort`

Коефіцієнт прискорення для короткого спрямування. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

`accelerationMaxShort`

Максимальне значення коефіцієнта прискорення для короткого спрямування. Допустимий діапазон від 0 до [TRADERREALMAX](trader.constants.html#constant.trader-real-max)

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.