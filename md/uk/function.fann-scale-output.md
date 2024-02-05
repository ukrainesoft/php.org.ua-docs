---
navigation:
  - function.fann-scale-output-train-data.md: « fann\_scale\_output\_train\_data
  - function.fann-scale-train-data.md: fann\_scale\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_scale\_output
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_scale\_output

(PECL fann >= 1.0.0)

fann\_scale\_output - Масштабує дані у вихідному векторі перед їх передачею в ann на основі раніше розрахованих параметрів

### Опис

```methodsynopsis
fann_scale_output(resource $ann, array $output_vector): bool
```

Масштабує дані у вихідному векторі перед їхньою передачею в ann на основі раніше розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`output_vector`

Вихідний вектор, який масштабується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_descale\_output()](function.fann-descale-output.md) \- Масштабує дані у вихідному векторі після отримання їх на основі раніше розрахованих параметрів
-   [fann\_scale\_input()](function.fann-scale-input.md) \- Масштабує дані у вхідному векторі перед подачею їх у ann на основі раніше розрахованих параметрів
