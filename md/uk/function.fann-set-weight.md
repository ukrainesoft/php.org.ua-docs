---
navigation:
  - function.fann-set-weight-array.md: « fann\_set\_weight\_array
  - function.fann-shuffle-train-data.md: fann\_shuffle\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_weight
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_weight

(PECL fann >= 1.0.0)

fann\_set\_weight — Створення зв'язку в мережі

### Опис

```methodsynopsis
fann_set_weight(    resource $ann,    int $from_neuron,    int $to_neuron,    float $weight): bool
```

Створює зв'язок у мережі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`from_neuron`

Початковий нейрон

`to_neuron`

Кінцевий нейрон

`weight`

Вага зв'язку

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.
