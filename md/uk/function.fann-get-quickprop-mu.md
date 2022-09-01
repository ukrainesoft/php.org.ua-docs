---
navigation:
  - function.fann-get-quickprop-decay.html: « fanngetquickpropdecay
  - function.fann-get-rprop-decrease-factor.html: fanngetrpropdecreasefactor »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetquickpropму
---
# fanngetquickpropму

(PECL fann> = 1.0.0)

fanngetquickpropmu — Повертає коефіцієнт mu

### Опис

```methodsynopsis
fann_get_quickprop_mu(resource $ann): float
```

Коефіцієнт mu використовується для збільшення та зменшення розміру кроку під час швидкого тренування. Коефіцієнт mu завжди повинен бути більшим за 1, оскільки в іншому випадку розмір кроку зменшиться, коли передбачається його збільшити.

Коефіцієнт mu за умовчанням дорівнює 1.75.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Коефіцієнт mu або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetquickpropmu()](function.fann-set-quickprop-mu.html) - Встановлює МЮ-фактор quickprop
