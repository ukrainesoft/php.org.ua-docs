---
navigation:
  - function.fann-init-weights.html: « fanninitweights
  - function.fann-merge-train-data.html: fannmergetraindata »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannlengthtraindata
---
# fannlengthtraindata

(PECL fann> = 1.0.0)

fannlengthtraindata — Повертає кількість шаблонів до навчальних даних

### Опис

```methodsynopsis
fann_length_train_data(resource $data): int
```

Повертає кількість шаблонів у ресурсі (resource) навчальних даних.

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Кількість елементів у ресурсі (resource) навчальних даних або **`false`** у разі виникнення помилки.
