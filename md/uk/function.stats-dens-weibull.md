Щільність ймовірності розподілу Вейбулла

-   [« stats\_dens\_uniform](function.stats-dens-uniform.html)
    
-   [stats\_harmonic\_mean »](function.stats-harmonic-mean.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Щільність ймовірності розподілу Вейбулла
    

# statsdensweibull

(PECL stats >= 1.0.0)

statsdensweibull - Щільність ймовірності розподілу Вейбулла

### Опис

```methodsynopsis
stats_dens_weibull(float $x, float $a, float $b): float
```

Повертає щільність ймовірності для `x`, де `a` і `b` є параметром форми та масштабним параметром відповідно.

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`a`

Параметр форми

`b`

Масштабний параметр розподілу

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.