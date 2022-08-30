Щільність ймовірності гамма-розподілу

-   [« statsdensф](function.stats-dens-f.html)
    
-   [statsdenslaplace »](function.stats-dens-laplace.html)
    
-   [PHP Manual](index.html)
    
-   [Функції статистики](ref.stats.html)
    
-   Щільність ймовірності гамма-розподілу
    

# statsdensgamma

(PECL stats >= 1.0.0)

statsdensgamma - Щільність ймовірності гамма-розподілу

### Опис

```methodsynopsis
stats_dens_gamma(float $x, float $shape, float $scale): float
```

Повертає щільність ймовірності для `x`, де `shape` і `scale` є коефіцієнтом форми та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`shape`

Параметр форми

`scale`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.