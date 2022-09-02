---
navigation:
  - function.fann-set-training-algorithm.md: « fannsettrainingalgorithm
  - function.fann-set-weight.md: fannsetweight »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetweightarray
---
# fannsetweightarray

(PECL fann> = 1.0.0)

fannsetweightarray — Створення зв'язків у мережі

### Опис

```methodsynopsis
fann_set_weight_array(resource $ann, array $connections): bool
```

Створення зв'язків у мережі.

Можуть бути змінені лише вагові коефіцієнти, що не існують у мережі зв'язку та ваги ігноруватимуться.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`connections`

Масив об'єктів [FANNConnection](class.fannconnection.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.
