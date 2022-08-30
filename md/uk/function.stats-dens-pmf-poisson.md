Імовірнісний захід розподілу Пуассона

-   [« statsdenspmfnegativebinomial](function.stats-dens-pmf-negative-binomial.html)
    
-   [statsdenst »](function.stats-dens-t.html)
    
-   [PHP Manual](index.html)
    
-   [Функції статистики](ref.stats.html)
    
-   Імовірнісний захід розподілу Пуассона
    

# statsdenspmfpoisson

(PECL stats >= 1.0.0)

statsdenspmfpoisson - Імовірнісний захід розподілу Пуассона

### Опис

```methodsynopsis
stats_dens_pmf_poisson(float $x, float $lb): float
```

Повертає імовірнісний захід для `x`, де `lb` є параметром розподілу Пуассона.

### Список параметрів

`x`

Значення, для якого вважається щільність ймовірності

`lb`

Параметр розподілу Пуассона

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.