---
navigation:
  - function.fann-set-weight-array.md: « fannsetweightarray
  - function.fann-shuffle-train-data.md: fannshuffletraindata »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetweight
---
# fannsetweight

(PECL fann> = 1.0.0)

fannsetweight — Створення зв'язку в мережі

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
