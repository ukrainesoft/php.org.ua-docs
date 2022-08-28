Щільність ймовірності розподілу Коші

-   [« stats\_dens\_beta](function.stats-dens-beta.html)
    
-   [stats\_dens\_chisquare »](function.stats-dens-chisquare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Щільність ймовірності розподілу Коші
    

# statsdenscauchy

(PECL stats >= 1.0.0)

statsdenscauchy — Щільність ймовірності розподілу Коші

### Опис

```methodsynopsis
stats_dens_cauchy(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності для `x`, де `ave` і `stdev` є коефіцієнтом зсуву та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність ймовірності

`ave`

Коефіцієнт зсуву

`stdev`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.