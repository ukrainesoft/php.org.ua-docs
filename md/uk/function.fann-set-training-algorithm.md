Встановлює алгоритм навчання

-   [« fannsettrainstopfunction](function.fann-set-train-stop-function.html)
    
-   [fannsetweightarray »](function.fann-set-weight-array.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює алгоритм навчання
    

# fannsettrainingalgorithm

(PECL fann> = 1.0.0)

fannsettrainingalgorithm - Встановлює алгоритм навчання

### Опис

```methodsynopsis
fann_set_training_algorithm(resource $ann, int $training_algorithm): bool
```

Встановлює алгоритм навчання.

Докладніша інформація доступна в [fanngettrainingalgorithm()](function.fann-get-training-algorithm.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`training_algorithm`

Константа [Алгоритма обучения](fann.constants.html#constants.fann-train)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngettrainingalgorithm()](function.fann-get-training-algorithm.html) - Повертає алгоритм навчання