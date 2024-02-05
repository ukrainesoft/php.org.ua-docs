---
navigation:
  - function.fann-scale-input.md: « fann\_scale\_input
  - function.fann-scale-output.md: fann\_scale\_output »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_scale\_output\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_scale\_output\_train\_data

(PECL fann >= 1.0.0)

fann\_scale\_output\_train\_data — Масштабує вихідні дані в навчальних даних до вказаного діапазону

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

-   [fann\_scale\_input\_train\_data()](function.fann-scale-input-train-data.md) \- Масштабує вхідні дані до навчальних даних до вказаного діапазону
-   [fann\_scale\_train\_data()](function.fann-scale-train-data.md) \- Масштабує вхідні та вихідні дані у навчальних даних до вказаного діапазону
