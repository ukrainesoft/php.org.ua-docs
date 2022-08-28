Імовірнісний захід гіпергеометричного розподілу

-   [« stats\_dens\_pmf\_binomial](function.stats-dens-pmf-binomial.html)
    
-   [stats\_dens\_pmf\_negative\_binomial »](function.stats-dens-pmf-negative-binomial.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Імовірнісний захід гіпергеометричного розподілу
    

# statsdenspmfhypergeometric

(PECL stats >= 1.0.0)

statsdenspmfhypergeometric - Імовірнісний захід гіпергеометричного розподілу

### Опис

```methodsynopsis
stats_dens_pmf_hypergeometric(    float $n1,    float $n2,    float $N1,    float $N2): float
```

Повертає імовірнісний захід для `n1`, де `n2` `N1` і `N2` є кількістю невдалих спроб, числом успішних вибірок та числом невдалих вибірок відповідно.

### Список параметрів

`n1`

Число успішних спроб, при яких обчислюється імовірнісний захід

`n2`

Кількість невдалих спроб

`N1`

Число успішних вибірок

`N2`

Число невдалих вибірок

### Значення, що повертаються

Імовірнісний захід для `n1` або **`false`** у разі виникнення помилки.