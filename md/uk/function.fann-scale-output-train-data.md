---
navigation:
  - function.fann-scale-input.html: « fannscaleinput
  - function.fann-scale-output.html: fannscaleoutput »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannscaleoutputtraindata
---
# fannscaleoutputtraindata

(PECL fann> = 1.0.0)

fannscaleoutputtraindata — Масштабує вихідні дані в навчальних даних до вказаного діапазону

### Опис

```methodsynopsis
fann_scale_output_train_data(resource $train_data, float $new_min, float $new_max): bool
```

Масштабує вихідні дані у навчальних даних до вказаного діапазону.

### Список параметрів

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_min`

Новий мінімум після масштабування вихідних даних у навчальних даних.

`new_max`

Новий максимум після масштабування вихідних даних у навчальних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannscaleinputtraindata()](function.fann-scale-input-train-data.html) - Масштабує вхідні дані до навчальних даних до вказаного діапазону
-   [fannscaletraindata()](function.fann-scale-train-data.html) - Масштабує вхідні та вихідні дані в навчальних даних до вказаного діапазону
