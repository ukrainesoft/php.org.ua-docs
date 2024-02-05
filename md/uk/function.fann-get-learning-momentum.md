---
navigation:
  - function.fann-get-layer-array.md: « fann\_get\_layer\_array
  - function.fann-get-learning-rate.md: fann\_get\_learning\_rate »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_learning\_momentum
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_learning\_momentum

(PECL fann >= 1.0.0)

fann\_get\_learning\_momentum - Повертає імпульс навчання

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

Импульс обучения или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_learning\_momentum()](function.fann-set-learning-momentum.md) \- встановлює імпульс навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
