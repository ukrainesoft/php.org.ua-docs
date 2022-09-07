---
navigation:
  - function.fann-set-learning-rate.md: « fannsetlearningrate
  - function.fann-set-quickprop-decay.md: fannsetquickpropdecay »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetoutputscalingparams
---
# fannsetoutputscalingparams

(PECL fann> = 1.0.0)

fannsetoutputscalingparams — Розраховує вихідні параметри масштабування для майбутнього використання на основі даних навчання

### Опис

```methodsynopsis
fann_set_output_scaling_params(    resource $ann,    resource $train_data,    float $new_output_min,    float $new_output_max): bool
```

Розраховує вихідні параметри масштабування майбутнього використання з урахуванням даних навчання.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_output_min`

Бажана нижня межа у вихідних даних після масштабування (суворо не дотримується)

`new_output_max`

Бажана верхня межа у вихідних даних після масштабування (суворо не дотримується)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetinputscalingparams()](function.fann-set-input-scaling-params.md) - розраховує вхідні параметри масштабування для майбутнього використання на основі даних навчання
