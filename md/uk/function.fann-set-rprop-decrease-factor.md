---
navigation:
  - function.fann-set-quickprop-mu.md: « fann\_set\_quickprop\_mu
  - function.fann-set-rprop-delta-max.md: fann\_set\_rprop\_delta\_max »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_rprop\_decrease\_factor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_rprop\_decrease\_factor

(PECL fann >= 1.0.0)

fann\_set\_rprop\_decrease\_factor — Встановлює коефіцієнт зменшення під час навчання RPROP

### Опис

```methodsynopsis
fann_set_rprop_decrease_factor(resource $ann, float $rprop_decrease_factor): bool
```

Встановлює коефіцієнт зменшення під час навчання RPROP.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_decrease_factor`

Коефіцієнт зменшення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_rprop\_decrease\_factor()](function.fann-get-rprop-decrease-factor.md) \- Повертає коефіцієнт зменшення під час навчання RPROP
