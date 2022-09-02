---
navigation:
  - function.fann-shuffle-train-data.md: « fannshuffletraindata
  - function.fann-test-data.md: fanntestdata »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsubsettraindata
---
# fannsubsettraindata

(PECL fann> = 1.0.0)

fannsubsettraindata — Отримати копію підмножини з навчальних даних

### Опис

```methodsynopsis
fann_subset_train_data(resource $data, int $pos, int $length): resource
```

Повертає копію підмножини з навчальних даних resource, що починаються з `pos` та довжиною `length` елементів.

`fann_subset_train_data(train_data, 0, fann_length_train_data(train_data))` робить те саме, що і [fannduplicatetraindata()](function.fann-duplicate-train-data.md)

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

`pos`

Початкова позиція.

`length`

Кількість елементів, що копіюються.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannduplicatetraindata()](function.fann-duplicate-train-data.md) - Повертає точну копію тренувальних даних
