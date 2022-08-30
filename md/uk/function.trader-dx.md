Індекс спрямованого руху

-   [« traderdiv](function.trader-div.html)
    
-   [traderema »](function.trader-ema.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Індекс спрямованого руху
    

# traderдкс

(PECL trader >= 0.2.0)

traderdx - Індекс спрямованого руху

### Опис

```methodsynopsis
trader_dx(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`timePeriod`

Номер періоду. Допустимі значення від 2 до 100000.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.