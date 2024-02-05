---
navigation:
  - function.fann-print-error.md: « fann\_print\_error
  - function.fann-read-train-from-file.md: fann\_read\_train\_from\_file »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_randomize\_weights
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_randomize\_weights

(PECL fann >= 1.0.0)

fann\_randomize\_weights — Надає кожному з'єднанню випадкову вагу між min\_weight та max\_weight

### Опис

```methodsynopsis
fann_randomize_weights(resource $ann, float $min_weight, float $max_weight): bool
```

Надає кожному з'єднанню випадкову вагу між `min_weight`и`max_weight`

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

-   [fann\_init\_weights()](function.fann-init-weights.md) \- Ініціалізує ваги за допомогою алгоритму Widrow + Nguyen
