---
navigation:
  - function.fann-get-rprop-delta-zero.md: « fann\_get\_rprop\_delta\_zero
  - function.fann-get-sarprop-step-error-shift.md: fann\_get\_sarprop\_step\_error\_shift »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_rprop\_increase\_factor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_rprop\_increase\_factor

(PECL fann >= 1.0.0)

fann\_get\_rprop\_increase\_factor — Повертає коефіцієнт збільшення під час навчання RPROP

### Опис

```methodsynopsis
fann_get_rprop_increase_factor(resource $ann): float
```

Коефіцієнт збільшення – це значення більше 1, яке використовується для збільшення розміру кроку під час навчання RPROP.

Коефіцієнт збільшення за умовчанням становить 1.2.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Коефіцієнт збільшення або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_rprop\_increase\_factor()](function.fann-set-rprop-increase-factor.md) \- Встановлює коефіцієнт збільшення, який використовується під час навчання Rprop
