---
navigation:
  - function.fann-set-quickprop-decay.md: « fann\_set\_quickprop\_decay
  - function.fann-set-rprop-decrease-factor.md: fann\_set\_rprop\_decrease\_factor »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_quickprop\_mu
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_quickprop\_mu

(PECL fann >= 1.0.0)

fann\_set\_quickprop\_mu - Встановлює МЮ-фактор quickprop

### Опис

```methodsynopsis
fann_set_quickprop_mu(resource $ann, float $quickprop_mu): bool
```

Встановлює МЮ-фактор quickprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`quickprop_mu`

МЮ-фактор quickprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_quickprop\_mu()](function.fann-get-quickprop-mu.md) \- Повертає коефіцієнт mu
