Імовірнісні заходи біномінального розподілу

-   [« stats\_dens\_normal](function.stats-dens-normal.html)
    
-   [stats\_dens\_pmf\_hypergeometric »](function.stats-dens-pmf-hypergeometric.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Імовірнісні заходи біномінального розподілу
    

# statsdenspmfbinomial

(PECL stats >= 1.0.0)

statsdenspmfbinomial - Імовірнісний захід біномінального розподілу

### Опис

```methodsynopsis
stats_dens_pmf_binomial(float $x, float $n, float $pi): float
```

Повертає щільність ймовірності для `x`, де `n` і `pi` є кількістю спроб та коефіцієнтом успішності відповідно.

### Список параметрів

`x`

Значення, для якого вважається імовірнісний захід

`n`

Кількість випробувань

`pi`

Коефіцієнт успішності

### Значення, що повертаються

Імовірнісний захід для `x` або **`false`** у разі виникнення помилки.