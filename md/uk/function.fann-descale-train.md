---
navigation:
  - function.fann-descale-output.md: « fann\_descale\_output
  - function.fann-destroy-train.md: fann\_destroy\_train »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_descale\_train
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_descale\_train

(PECL fann >= 1.0.0)

fann\_descale\_train — Масштабування вхідних та вихідних даних на основі попередньо розрахованих параметрів

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

-   [fann\_scale\_train()](function.fann-scale-train.md) \- Масштабує вхідні та вихідні дані на основі раніше розрахованих параметрів
-   [fann\_set\_scaling\_params()](function.fann-set-scaling-params.md) \- Розраховує вхідні та вихідні параметри масштабування для майбутнього використання на основі даних навчання
