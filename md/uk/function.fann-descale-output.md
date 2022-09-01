---
navigation:
  - function.fann-descale-input.html: « fanndescaleinput
  - function.fann-descale-train.html: fanndescaletrain »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanndescaleoutput
---
# fanndescaleoutput

(PECL fann> = 1.0.0)

fanndescaleoutput — Масштабує дані у вихідному векторі після отримання їх на основі раніше розрахованих параметрів

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

-   [fannscaleoutput()](function.fann-scale-output.md) - Масштабує дані у вихідному векторі перед їх передачею в ann на основі раніше розрахованих параметрів
-   [fanndescaleinput()](function.fann-descale-input.md) - Масштабує дані у вхідному векторі після отримання їх на основі раніше розрахованих параметрів
