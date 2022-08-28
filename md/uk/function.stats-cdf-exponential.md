Обчислює один із параметрів експоненційного розподілу за рештою

-   [« stats\_cdf\_chisquare](function.stats-cdf-chisquare.html)
    
-   [stats\_cdf\_f »](function.stats-cdf-f.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Обчислює один із параметрів експоненційного розподілу за рештою
    

# statscdfexponential

(PECL stats >= 1.0.0)

statscdfexponential — Обчислює один із параметрів експоненційного розподілу за рештою

### Опис

```methodsynopsis
stats_cdf_exponential(float $par1, float $par2, int $which): float
```

Повертає кумулятивну функцію експоненціального розподілу, обернену до неї або один зі своїх параметрів. Вигляд значення і параметрів (`par1` і `par2`) визначаються параметром `which`

У наступній таблиці перераховані значення і параметри, що повертаються, в залежності від `which`. CDF, x і lambda позначає функцію кумулятивного розподілу, значення випадкової змінної та інтенсивність (зворотний коефіцієнт масштабу) відповідно.

**Значення, що повертається і параметри**

| `which` | Возвращаемое значение | `par1` | `par2` |
|---------|-----------------------|--------|--------|
|         | CDF                   | з      | lambda |
|         | з                     | CDF    | lambda |
|         | lambda                | з      | CDF    |

### Список параметрів

`par1`

Перший параметр

`par2`

Другий параметр

`which`

Прапор, що визначає, що буде повернено

### Значення, що повертаються

Повертає CDF, x або lambda, залежно від значення `which`