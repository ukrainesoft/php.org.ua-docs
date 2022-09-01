---
navigation:
  - function.fann-get-layer-array.html: « fanngetlayerarray
  - function.fann-get-learning-rate.html: fanngetlearningrate »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetlearningmomentum
---
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

-   [fannsetlearningmomentum()](function.fann-set-learning-momentum.html) - встановлює імпульс навчання
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання
