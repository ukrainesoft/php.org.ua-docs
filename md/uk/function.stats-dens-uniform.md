Функція густини ймовірності рівномірного розподілу

-   [« stats\_dens\_t](function.stats-dens-t.html)
    
-   [stats\_dens\_weibull »](function.stats-dens-weibull.html)
    
-   [PHP Manual](index.html)
    
-   [Функции статистики](ref.stats.html)
    
-   Функція густини ймовірності рівномірного розподілу
    

# statsdensuniform

(PECL stats >= 1.0.0)

statsdensuniform - Функція щільності ймовірності рівномірного розподілу

### Опис

```methodsynopsis
stats_dens_uniform(float $x, float $a, float $b): float
```

Повертає щільність ймовірності у `x`, де нижня межа задана в `a`, а верхня в `b`

### Список параметрів

`x`

Значення якого обчислюватиметься щільність ймовірності

`a`

Нижній кордон розподілу

`b`

Верхня межа розподілу

### Значення, що повертаються

Щільність ймовірності в `x` або **`false`** у разі виникнення помилки.