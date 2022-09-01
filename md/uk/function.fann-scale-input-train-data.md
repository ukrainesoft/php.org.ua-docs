---
navigation:
  - function.fann-save.html: « fannsave
  - function.fann-scale-input.html: fannscaleinput »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannscaleinputtraindata
---
# fannscaleinputtraindata

(PECL fann> = 1.0.0)

fannscaleinputtraindata — Масштабує вхідні дані до навчальних даних до вказаного діапазону

### Опис

```methodsynopsis
fann_scale_input_train_data(resource $train_data, float $new_min, float $new_max): bool
```

Масштабує вхідні дані до навчальних даних до вказаного діапазону.

### Список параметрів

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_min`

Новий мінімум після масштабування вхідних даних до навчальних даних.

`new_max`

Новий максимум після масштабування вхідних даних до навчальних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannscaleoutputtraindata()](function.fann-scale-output-train-data.md) - Масштабує вихідні дані у навчальних даних до вказаного діапазону
-   [fannscaletraindata()](function.fann-scale-train-data.md) - Масштабує вхідні та вихідні дані у навчальних даних до вказаного діапазону
