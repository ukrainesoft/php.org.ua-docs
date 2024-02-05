---
navigation:
  - function.fann-get-quickprop-mu.md: « fann\_get\_quickprop\_mu
  - function.fann-get-rprop-delta-max.md: fann\_get\_rprop\_delta\_max »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_rprop\_decrease\_factor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_rprop\_decrease\_factor

(PECL fann >= 1.0.0)

fann\_get\_rprop\_decrease\_factor — Повертає коефіцієнт зменшення під час навчання RPROP

### Опис

```methodsynopsis
fann_get_rprop_decrease_factor(resource $ann): float
```

Коефіцієнт зменшення це значення менше 1, яке використовується для зменшення розміру кроку під час навчання RPROP.

Коефіцієнт зменшення за промовчанням становить 0.5.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Коефіцієнт зменшення або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_rprop\_decrease\_factor()](function.fann-set-rprop-decrease-factor.md) \- Встановлює коефіцієнт зменшення під час навчання RPROP
