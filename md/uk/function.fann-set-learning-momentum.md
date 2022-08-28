Встановлює імпульс навчання

-   [« fann\_set\_input\_scaling\_params](function.fann-set-input-scaling-params.html)
    
-   [fann\_set\_learning\_rate »](function.fann-set-learning-rate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює імпульс навчання
    

# fannsetlearningmomentum

(PECL fann> = 1.0.0)

fannsetlearningmomentum - Встановлює імпульс навчання

### Опис

```methodsynopsis
fann_set_learning_momentum(resource $ann, float $learning_momentum): bool
```

Встановлює імпульс навчання.

Докладніша інформація доступна в [fann\_get\_learning\_momentum()](function.fann-get-learning-momentum.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`learning_momentum`

Імпульс навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_learning\_momentum()](function.fann-get-learning-momentum.html) - Повертає імпульс навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання