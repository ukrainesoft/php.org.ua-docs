Обчислює один із параметрів розподілу Коші за рештою

-   [« stats\_cdf\_binomial](function.stats-cdf-binomial.html)
    
-   [stats\_cdf\_chisquare »](function.stats-cdf-chisquare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Обчислює один із параметрів розподілу Коші за рештою
    

# statscdfcauchy

(PECL stats >= 1.0.0)

statscdfcauchy — Обчислює один із параметрів розподілу Коші за іншими

### Опис

```methodsynopsis
stats_cdf_cauchy(    float $par1,    float $par2,    float $par3,    int $which): float
```

Повертає кумулятивну функцію розподілу Коші, обернену їй або один із своїх параметрів. Вигляд значення і параметрів (`par1` `par2` і `par3`) визначаються параметром `which`

У наступній таблиці перераховані значення, що повертаються, і параметри в залежності від `which`. CDF, x, x0 та gamma позначає функцію кумулятивного розподілу, значення випадкової змінної, параметр зсуву та масштабу відповідно.

**Значення, що повертається, та параметри**

| `which` | Возвращаемое значение | `par1` | `par2` | `par3` |
|---------|-----------------------|--------|--------|--------|
|         | CDF                   | з      | кс0    | gamma  |
|         | з                     | CDF    | кс0    | gamma  |
|         | кс0                   | з      | CDF    | gamma  |
|         | gamma                 | з      | CDF    | кс0    |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`par3`

Третій параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x, x0 або gamma залежно від значення `which`