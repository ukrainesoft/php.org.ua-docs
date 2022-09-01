---
navigation:
  - function.fann-num-input-train-data.html: « fannnuminputtraindata
  - function.fann-print-error.html: fannprinterror »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannnumoutputtraindata
---
# fannnumoutputtraindata

(PECL fann> = 1.0.0)

fannnumoutputtraindata — Повертає кількість вихідних даних у кожному із шаблонів у навчальних даних

### Опис

```methodsynopsis
fann_num_output_train_data(resource $data): int
```

Повертає кількість вихідних даних у кожному із шаблонів у ресурсі (resource) навчальних даних.

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Кількість вихідних даних або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannlengthtraindata()](function.fann-length-train-data.md) - Повертає кількість шаблонів у навчальних даних
-   [fannnuminputtraindata()](function.fann-num-input-train-data.md) - Повертає кількість вхідних даних у кожному із шаблонів у навчальних даних
