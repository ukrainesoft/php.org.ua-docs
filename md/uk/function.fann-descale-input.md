---
navigation:
  - function.fann-create-train.md: « fann\_create\_train
  - function.fann-descale-output.md: fann\_descale\_output »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_descale\_input
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_descale\_input

(PECL fann >= 1.0.0)

fann\_descale\_input — Масштабує дані у вхідному векторі після отримання на основі раніше розрахованих параметрів

### Опис

```methodsynopsis
fann_descale_input(resource $ann, array $input_vector): bool
```

Масштабує дані у вхідному векторі після отримання на основі раніше розрахованих параметрів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input_vector`

Вхідний вектор, який буде масштабовано

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_scale\_input()](function.fann-scale-input.md) \- Масштабує дані у вхідному векторі перед подачею їх у ann на основі раніше розрахованих параметрів
-   [fann\_descale\_output()](function.fann-descale-output.md) \- Масштабує дані у вихідному векторі після отримання їх на основі раніше розрахованих параметрів
