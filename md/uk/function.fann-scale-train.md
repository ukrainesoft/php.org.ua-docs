---
navigation:
  - function.fann-scale-train-data.md: « fann\_scale\_train\_data
  - function.fann-set-activation-function-hidden.md: fann\_set\_activation\_function\_hidden »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_scale\_train
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_scale\_train

(PECL fann >= 1.0.0)

fann\_scale\_train — Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів

### Опис

```methodsynopsis
fann_scale_train(resource $ann, resource $train_data): bool
```

Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_descale\_train()](function.fann-descale-train.md) \- Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів
-   [fann\_set\_scaling\_params()](function.fann-set-scaling-params.md) \- Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання
