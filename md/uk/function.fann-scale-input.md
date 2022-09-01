---
navigation:
  - function.fann-scale-input-train-data.html: « fannscaleinputtraindata
  - function.fann-scale-output-train-data.html: fannscaleoutputtraindata »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannscaleinput
---
# fannscaleinput

(PECL fann> = 1.0.0)

fannscaleinput — Масштабує дані у вхідному векторі перед подачею в ann на основі раніше розрахованих параметрів

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

-   [fanndescaleinput()](function.fann-descale-input.html) - Масштабує дані у вхідному векторі після отримання їх на основі раніше розрахованих параметрів
-   [fannscaleoutput()](function.fann-scale-output.html) - Масштабує дані у вихідному векторі перед їх передачею в ann на основі раніше розрахованих параметрів
