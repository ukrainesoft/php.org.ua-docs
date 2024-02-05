---
navigation:
  - function.fann-save.md: « fann\_save
  - function.fann-scale-input.md: fann\_scale\_input »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_scale\_input\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_scale\_input\_train\_data

(PECL fann >= 1.0.0)

fann\_scale\_input\_train\_data — Масштабує вхідні дані до навчальних даних до вказаного діапазону

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

-   [fann\_scale\_output\_train\_data()](function.fann-scale-output-train-data.md) \- Масштабує вихідні дані у навчальних даних до вказаного діапазону
-   [fann\_scale\_train\_data()](function.fann-scale-train-data.md) \- Масштабує вхідні та вихідні дані у навчальних даних до вказаного діапазону
