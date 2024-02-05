---
navigation:
  - function.fann-set-training-algorithm.md: « fann\_set\_training\_algorithm
  - function.fann-set-weight.md: fann\_set\_weight »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_weight\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_weight\_array

(PECL fann >= 1.0.0)

fann\_set\_weight\_array — Створення зв'язків у мережі

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
