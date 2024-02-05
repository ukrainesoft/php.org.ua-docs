---
navigation:
  - function.fann-get-quickprop-decay.md: « fann\_get\_quickprop\_decay
  - function.fann-get-rprop-decrease-factor.md: fann\_get\_rprop\_decrease\_factor »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_quickprop\_mu
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_quickprop\_mu

(PECL fann >= 1.0.0)

fann\_get\_quickprop\_mu — Повертає коефіцієнт mu

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

Коефіцієнт mu або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_quickprop\_mu()](function.fann-set-quickprop-mu.md) \- Встановлює МЮ-фактор quickprop
