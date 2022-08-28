Повертає імпульс навчання

-   [« fann\_get\_layer\_array](function.fann-get-layer-array.html)
    
-   [fann\_get\_learning\_rate »](function.fann-get-learning-rate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає імпульс навчання
    

# fanngetlearningmomentum

(PECL fann> = 1.0.0)

fanngetlearningmomentum - Повертає імпульс навчання

### Опис

```methodsynopsis
fann_get_learning_momentum(resource $ann): float
```

Імпульс навчання можна використовувати для прискорення навчання **`FANN_TRAIN_INCREMENTAL`**. Проте надто високий імпульс не принесе користі тренуванням. Встановлення імпульсу на 0 буде рівним відключенню параметра імпульсу. Цей параметр рекомендується від 0.0 до 1.0.

Імпульс за замовчуванням дорівнює 0.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

Імпульс навчання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_learning\_momentum()](function.fann-set-learning-momentum.html) - встановлює імпульс навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання