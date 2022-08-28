Повертає функцію зупинки, що використовується під час навчання

-   [« fann\_get\_train\_error\_function](function.fann-get-train-error-function.html)
    
-   [fann\_get\_training\_algorithm »](function.fann-get-training-algorithm.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає функцію зупинки, що використовується під час навчання
    

# fanngettrainstopfunction

(PECL fann> = 1.0.0)

fanngettrainstopfunction — Повертає функцію зупинки, що використовується під час навчання

### Опис

```methodsynopsis
fann_get_train_stop_function(resource $ann): int
```

Повертає функцію зупинки під час навчання.

Опції зупинки описані далі в константах [функции остановки](fann.constants.html#constants.fann-stopfunc)

За замовчуванням функція зупинки: **`FANN_STOPFUNC_MSE`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа [функции остановки](fann.constants.html#constants.fann-stopfunc) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.html) - Встановлює функцію зупинки під час тренування.