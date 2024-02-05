---
navigation:
  - function.fann-descale-input.md: « fann\_descale\_input
  - function.fann-descale-train.md: fann\_descale\_train »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_descale\_output
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_descale\_output

(PECL fann >= 1.0.0)

fann\_descale\_output — Масштабує дані у вихідному векторі після отримання їх на основі раніше розрахованих параметрів

### Опис

```methodsynopsis
fann_descale_output(resource $ann, array $output_vector): bool
```

Масштабує дані у вихідному векторі після отримання їх на основі раніше розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`output_vector`

Вихідний вектор, який буде масштабовано

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_scale\_output()](function.fann-scale-output.md) \- Масштабує дані у вихідному векторі перед їх передачею в ann на основі раніше розрахованих параметрів
-   [fann\_descale\_input()](function.fann-descale-input.md) \- Масштабує дані у вхідному векторі після отримання їх на основі раніше розрахованих параметрів
