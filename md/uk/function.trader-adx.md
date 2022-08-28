Середній індекс спрямованого руху

-   [« trader\_adosc](function.trader-adosc.html)
    
-   [trader\_adxr »](function.trader-adxr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   Середній індекс спрямованого руху
    

# traderadx

(PECL trader >= 0.2.0)

traderadx - Середній індекс спрямованого руху

### Опис

```methodsynopsis
trader_adx(    array $high,    array $low,    array $close,    int $timePeriod = ?): array
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