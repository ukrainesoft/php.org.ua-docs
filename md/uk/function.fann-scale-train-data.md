---
navigation:
  - function.fann-scale-output.md: « fannscaleoutput
  - function.fann-scale-train.md: fannscaletrain »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannscaletraindata
---
# fannscaletraindata

(PECL fann> = 1.0.0)

fannscaletraindata — Масштабує вхідні та вихідні дані в навчальних даних до вказаного діапазону

### Опис

```methodsynopsis
fann_scale_train_data(resource $train_data, float $new_min, float $new_max): bool
```

Масштабує вхідні та вихідні дані у навчальних даних до вказаного діапазону.

### Список параметрів

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_min`

Новий мінімум після масштабування вхідних та вихідних даних у навчальних даних.

`new_max`

Новий максимум після масштабування вхідних та вихідних даних у навчальних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannscaleoutputtraindata()](function.fann-scale-output-train-data.md) - Масштабує вихідні дані у навчальних даних до вказаного діапазону
-   [fannscaleinputtraindata()](function.fann-scale-input-train-data.md) - Масштабує вхідні дані до навчальних даних до вказаного діапазону
