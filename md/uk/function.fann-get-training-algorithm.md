Повертає алгоритм навчання

-   [« fann\_get\_train\_stop\_function](function.fann-get-train-stop-function.html)
    
-   [fann\_init\_weights »](function.fann-init-weights.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає алгоритм навчання
    

# fanngettrainingalgorithm

(PECL fann> = 1.0.0)

fanngettrainingalgorithm - Повертає алгоритм навчання

### Опис

```methodsynopsis
fann_get_training_algorithm(resource $ann): int
```

Повертає алгоритм навчання. Цей алгоритм навчання використовується [fann\_train\_on\_data()](function.fann-train-on-data.html) та пов'язаними функціями.

Зверніть увагу, що цей алгоритм також використовується під час [fann\_cascadetrain\_on\_data()](function.fann-cascadetrain-on-data.html), хоча під час каскадного навчання дозволено лише **`FANN_TRAIN_RPROP`** and **`FANN_TRAIN_QUICKPROP`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа [Алгоритма обучения](fann.constants.html#constants.fann-train) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання