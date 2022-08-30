Встановлює швидкість навчання

-   [« fannsetlearningmomentum](function.fann-set-learning-momentum.html)
    
-   [fannsetoutputscalingparams »](function.fann-set-output-scaling-params.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Встановлює швидкість навчання
    

# fannsetlearningrate

(PECL fann> = 1.0.0)

fannsetlearningrate — Встановлює швидкість навчання

### Опис

```methodsynopsis
fann_set_learning_rate(resource $ann, float $learning_rate): bool
```

Встановлює швидкість навчання.

Докладніша інформація доступна в [fanngetlearningrate()](function.fann-get-learning-rate.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`learning_rate`

Швидкість навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetlearningrate()](function.fann-get-learning-rate.html) - Повертає швидкість навчання
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання