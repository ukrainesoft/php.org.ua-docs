Встановлює функцію зупинки під час тренування.

-   [« fannsettrainerrorfunction](function.fann-set-train-error-function.html)
    
-   [fannsettrainingalgorithm »](function.fann-set-training-algorithm.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює функцію зупинки під час тренування.
    

# fannsettrainstopfunction

(PECL fann> = 1.0.0)

fannsettrainstopfunction — Встановлює функцію зупинки під час тренування.

### Опис

```methodsynopsis
fann_set_train_stop_function(resource $ann, int $stop_function): bool
```

Встановлює функцію зупинки під час тренування.

Функції зупинки описані далі в константах [функции остановки](fann.constants.html#constants.fann-stopfunc)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`stop_function`

Константа [функции остановки](fann.constants.html#constants.fann-stopfunc)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngettrainstopfunction()](function.fann-get-train-stop-function.html) - Повертає функцію зупинки, що використовується під час навчання