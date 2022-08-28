Щільність ймовірності логістичного розподілу

-   [« stats\_dens\_laplace](function.stats-dens-laplace.html)
    
-   [stats\_dens\_normal »](function.stats-dens-normal.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Щільність ймовірності логістичного розподілу
    

# statsdenslogistic

(PECL stats >= 1.0.0)

statsdenslogistic - Щільність ймовірності логістичного розподілу

### Опис

```methodsynopsis
stats_dens_logistic(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, де `ave` і `stdev` є коефіцієнтом зсуву та логістичним розподілом відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`ave`

Коефіцієнт зсуву

`stdev`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.