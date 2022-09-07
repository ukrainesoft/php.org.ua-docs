---
navigation:
  - function.fann-descale-output.md: « fanndescaleoutput
  - function.fann-destroy-train.md: fanndestroytrain »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanndescaletrain
---
# fanndescaletrain

(PECL fann> = 1.0.0)

fanndescaletrain — Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів

### Опис

```methodsynopsis
fann_descale_train(resource $ann, resource $train_data): bool
```

Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannscaletrain()](function.fann-scale-train.md) - Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів
-   [fannsetscalingparams()](function.fann-set-scaling-params.md) - Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання
