---
navigation:
  - function.fann-set-error-log.md: « fannseterrorlog
  - function.fann-set-learning-momentum.md: fannsetlearningmomentum »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetinputscalingparams
---
# fannsetinputscalingparams

(PECL fann> = 1.0.0)

fannsetinputscalingparams — Розраховує вхідні параметри масштабування для майбутнього використання на основі даних навчання

### Опис

```methodsynopsis
fann_set_input_scaling_params(    resource $ann,    resource $train_data,    float $new_input_min,    float $new_input_max): bool
```

Розраховує вхідні параметри масштабування майбутнього використання з урахуванням даних навчання.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

`new_input_min`

Бажана нижня межа у вхідних даних після масштабування (суворо не дотримується)

`new_input_max`

Бажана верхня межа у вхідних даних після масштабування (суворо не дотримується)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetoutputscalingparams()](function.fann-set-output-scaling-params.md) - розраховує вихідні параметри масштабування для майбутнього використання на основі даних навчання
