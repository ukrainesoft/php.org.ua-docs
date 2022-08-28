Щільність ймовірності розподілу Лапласа

-   [« stats\_dens\_gamma](function.stats-dens-gamma.html)
    
-   [stats\_dens\_logistic »](function.stats-dens-logistic.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Щільність ймовірності розподілу Лапласа
    

# statsdenslaplace

(PECL stats >= 1.0.0)

statsdenslaplace - Щільність ймовірності розподілу Лапласа

### Опис

```methodsynopsis
stats_dens_laplace(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, де `ave` і `stdev` є коефіцієнтом зсуву та параметром форми відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`ave`

Коефіцієнт зсуву

`stdev`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.