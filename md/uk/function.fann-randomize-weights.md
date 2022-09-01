---
navigation:
  - function.fann-print-error.html: « fannprinterror
  - function.fann-read-train-from-file.html: fannreadtrainfromfile »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannrandomizeweights
---
# fannrandomizeweights

(PECL fann> = 1.0.0)

fannrandomizeweights — Надає кожному з'єднанню випадкову вагу між minweight та maxweight

### Опис

```methodsynopsis
fann_randomize_weights(resource $ann, float $min_weight, float $max_weight): bool
```

Надає кожному з'єднанню випадкову вагу між `min_weight` і `max_weight`

З початку випадковий вага в діапазоні від -0,1 до 0,1.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`min_weight`

Мінімальне значення ваги.

`max_weight`

Максимальне значення ваги.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanninitweights()](function.fann-init-weights.html) - Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen
