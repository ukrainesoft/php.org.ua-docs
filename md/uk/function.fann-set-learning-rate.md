Встановлює швидкість навчання

-   [« fann\_set\_learning\_momentum](function.fann-set-learning-momentum.html)
    
-   [fann\_set\_output\_scaling\_params »](function.fann-set-output-scaling-params.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює швидкість навчання
    

# fannsetlearningrate

(PECL fann> = 1.0.0)

fannsetlearningrate — Встановлює швидкість навчання

### Опис

```methodsynopsis
fann_set_learning_rate(resource $ann, float $learning_rate): bool
```

Встановлює швидкість навчання.

Докладніша інформація доступна в [fann\_get\_learning\_rate()](function.fann-get-learning-rate.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`learning_rate`

Швидкість навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_learning\_rate()](function.fann-get-learning-rate.html) - Повертає швидкість навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання