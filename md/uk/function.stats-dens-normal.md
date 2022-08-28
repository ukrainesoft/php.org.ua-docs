Повертає щільність ймовірності нормального розподілу

-   [« stats\_dens\_logistic](function.stats-dens-logistic.html)
    
-   [stats\_dens\_pmf\_binomial »](function.stats-dens-pmf-binomial.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Повертає щільність ймовірності нормального розподілу
    

# statsdensnormal

(PECL stats >= 1.0.0)

statsdensnormal — Повертає щільність ймовірності нормального розподілу

### Опис

```methodsynopsis
stats_dens_normal(float $x, float $ave, float $stdev): float
```

Повертає щільність ймовірності при `x`, де випадкова величина слідує за нормальним розподілом, середнє значення якого `ave` та стандартне відхилення `stdev`

### Список параметрів

`x`

Величина, для якої обчислюється щільність імовірності

`ave`

Середнє значення розподілу

`stdev`

Стандартне відхилення

### Значення, що повертаються

Щільність ймовірності для `x` або **`false`** у разі виникнення помилки.