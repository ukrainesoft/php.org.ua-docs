---
navigation:
  - function.fann-length-train-data.md: « fannlengthtraindata
  - function.fann-num-input-train-data.md: fannnuminputtraindata »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannmergetraindata
---
# fannmergetraindata

(PECL fann> = 1.0.0)

fannmergetraindata — Об'єднує навчальні дані

### Опис

```methodsynopsis
fann_merge_train_data(resource $data1, resource $data2): resource
```

Об'єднує дані з data1 і data2 у новий ресурс (resource) навчальних даних.

### Список параметрів

`data1`

Ресурс (resource) навчальних даних нейронної мережі.

`data2`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Новий ресурс (resource) об'єднаних навчальних даних або **`false`** у разі виникнення помилки.
