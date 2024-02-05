---
navigation:
  - function.fann-set-rprop-delta-zero.md: « fann\_set\_rprop\_delta\_zero
  - function.fann-set-sarprop-step-error-shift.md: fann\_set\_sarprop\_step\_error\_shift »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_rprop\_increase\_factor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_rprop\_increase\_factor

(PECL fann >= 1.0.0)

fann\_set\_rprop\_increase\_factor — Встановлює коефіцієнт збільшення, який використовується під час навчання Rprop

### Опис

```methodsynopsis
fann_set_rprop_increase_factor(resource $ann, float $rprop_increase_factor): bool
```

Встановлює коефіцієнт збільшення під час навчання Rprop

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_increase_factor`

Коефіцієнт збільшення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_rprop\_increase\_factor()](function.fann-get-rprop-increase-factor.md) \- Повертає коефіцієнт збільшення, який використовується під час навчання RPROP
