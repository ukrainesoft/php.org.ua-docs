---
navigation:
  - function.fann-merge-train-data.html: « fannmergetraindata
  - function.fann-num-output-train-data.html: fannnumoutputtraindata »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannnuminputtraindata
---
# fannnuminputtraindata

(PECL fann> = 1.0.0)

fannnuminputtraindata — Повертає кількість вхідних даних у кожному шаблоні до навчальних даних.

### Опис

```methodsynopsis
fann_num_input_train_data(resource $data): int
```

Повертає кількість вхідних даних у кожному із шаблонів у ресурсі (resource) навчальних даних.

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Кількість вхідних даних або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannlengthtraindata()](function.fann-length-train-data.md) - Повертає кількість шаблонів у навчальних даних
-   [fannnumoutputtraindata()](function.fann-num-output-train-data.md) - Повертає кількість вихідних даних у кожному із шаблонів у навчальних даних
