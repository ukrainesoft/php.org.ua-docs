---
navigation:
  - function.fann-scale-input-train-data.md: « fann\_scale\_input\_train\_data
  - function.fann-scale-output-train-data.md: fann\_scale\_output\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_scale\_input
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_scale\_input

(PECL fann >= 1.0.0)

fann\_scale\_input — Масштабує дані у вхідному векторі перед подачею в ann на основі раніше розрахованих параметрів

### Опис

```methodsynopsis
fann_scale_input(resource $ann, array $input_vector): bool
```

Масштабує дані у вхідному векторі перед подачею в ann на основі раніше розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input_vector`

Вхідний вектор масштабується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_descale\_input()](function.fann-descale-input.md) \- Масштабує дані у вхідному векторі після отримання їх на основі раніше розрахованих параметрів
-   [fann\_scale\_output()](function.fann-scale-output.md) \- Масштабує дані у вихідному векторі перед їх передачею в ann на основі раніше розрахованих параметрів
