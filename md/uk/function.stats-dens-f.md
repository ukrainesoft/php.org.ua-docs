Щільність ймовірності розподілу Фішера

-   [« stats\_dens\_exponential](function.stats-dens-exponential.html)
    
-   [stats\_dens\_gamma »](function.stats-dens-gamma.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Щільність ймовірності розподілу Фішера
    

# statsdensф

(PECL stats >= 1.0.0)

statsdensf - Щільність ймовірності розподілу Фішера

### Опис

```methodsynopsis
stats_dens_f(float $x, float $dfr1, float $dfr2): float
```

Повертає щільність ймовірності для `x`, де `dfr1` і `dfr2` відбивають ступеня свободи.

### Список параметрів

`x`

Значення, для якого вважається щільність ймовірності

`dfr1`

Ступені свободи

`dfr2`

Ступені свободи

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.