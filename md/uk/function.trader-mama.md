MESA Адаптивна ковзна середня

-   [« tradermacdfix](function.trader-macdfix.html)
    
-   [tradermavp »](function.trader-mavp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Trader](ref.trader.html)
    
-   MESA Адаптивна ковзна середня
    

# tradermama

(PECL trader >= 0.2.0)

tradermama — MESA Адаптивна ковзна середня

### Опис

```methodsynopsis
trader_mama(array $real, float $fastLimit = ?, float $slowLimit = ?): array
```

### Список параметрів

`real`

Масив, що містить реальні значення.

`fastLimit`

Верхня межа, яка використовується в адаптивному алгоритмі. Допустимі значення від 0.01 до 0.99.

`slowLimit`

Нижня межа, яка використовується в адаптивному алгоритмі. Допустимі значення від 0.01 до 0.99.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.