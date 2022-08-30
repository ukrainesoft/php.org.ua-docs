Встановлює імпульс навчання

-   [« fannsetinputscalingparams](function.fann-set-input-scaling-params.html)
    
-   [fannsetlearningrate »](function.fann-set-learning-rate.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Встановлює імпульс навчання
    

# fannsetlearningmomentum

(PECL fann> = 1.0.0)

fannsetlearningmomentum - Встановлює імпульс навчання

### Опис

```methodsynopsis
fann_set_learning_momentum(resource $ann, float $learning_momentum): bool
```

Встановлює імпульс навчання.

Докладніша інформація доступна в [fanngetlearningmomentum()](function.fann-get-learning-momentum.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`learning_momentum`

Імпульс навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetlearningmomentum()](function.fann-get-learning-momentum.html) - Повертає імпульс навчання
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання