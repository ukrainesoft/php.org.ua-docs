Щільність ймовірності бета-розподілу

-   [« statscovariance](function.stats-covariance.html)
    
-   [statsdenscauchy »](function.stats-dens-cauchy.html)
    
-   [PHP Manual](index.html)
    
-   [Функції статистики](ref.stats.html)
    
-   Щільність ймовірності бета-розподілу
    

# statsdensbeta

(PECL stats >= 1.0.0)

statsdensbeta - Щільність ймовірності бета-розподілу

### Опис

```methodsynopsis
stats_dens_beta(float $x, float $a, float $b): float
```

Повертає щільність ймовірності для `x`де де випадкова величина слідує за бета-розподілом, параметри форми якого є `a` і `b`

### Список параметрів

`x`

Значення, для якого вважається щільність імовірності

`a`

Параметр форми

`b`

Параметр форми

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`**, у разі виникнення помилки.