Повертає швидкість навчання

-   [« fann\_get\_learning\_momentum](function.fann-get-learning-momentum.html)
    
-   [fann\_get\_MSE »](function.fann-get-mse.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає швидкість навчання
    

# fanngetlearningrate

(PECL fann> = 1.0.0)

fanngetlearningrate — Повертає швидкість навчання

### Опис

```methodsynopsis
fann_get_learning_rate(resource $ann): float
```

Швидкість навчання використовується визначення того, наскільки агресивним має бути навчання деяких алгоритмів навчання (**`FANN_TRAIN_INCREMENTAL`** **`FANN_TRAIN_BATCH`** **`FANN_TRAIN_QUICKPROP`**). Однак зверніть увагу, що вона не використовується в **`FANN_TRAIN_RPROP`**

Швидкість навчання за замовчуванням дорівнює 0.7.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Швидкість навчання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_learning\_rate()](function.fann-set-learning-rate.html) - встановлює швидкість навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання