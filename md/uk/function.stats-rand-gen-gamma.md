Обчислює випадкове відхилення від гамма-розподілу

-   [« stats\_rand\_gen\_funiform](function.stats-rand-gen-funiform.html)
    
-   [stats\_rand\_gen\_ibinomial\_negative »](function.stats-rand-gen-ibinomial-negative.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Обчислює випадкове відхилення від гамма-розподілу
    

# statsrandгенgamma

(PECL stats >= 1.0.0)

statsrandгенgamma - Обчислює випадкове відхилення від гамма-розподілу

### Опис

```methodsynopsis
stats_rand_gen_gamma(float $a, float $r): float
```

Згенерувати випадкове відхилення від Гамма-розподілу. Щільність розраховується за формулою (AR)/Gamma(R) З(R-1) Exp(-AX).

### Список параметрів

`a`

Коефіцієнт зсуву Гамма-розподілу (`a` > 0).

`r`

Коефіцієнт форми Гамма-розподілу (`r` > 0).

### Значення, що повертаються

Випадкове відхилення