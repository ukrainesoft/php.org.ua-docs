---
navigation:
  - function.fann-set-sarprop-temperature.md: « fann\_set\_sarprop\_temperature
  - function.fann-set-scaling-params.md: fann\_set\_scaling\_params »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_sarprop\_weight\_decay\_shift
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_sarprop\_weight\_decay\_shift

(PECL fann >= 1.0.0)

fann\_set\_sarprop\_weight\_decay\_shift - Встановлює зміщення згасання sarprop

### Опис

```methodsynopsis
fann_set_sarprop_weight_decay_shift(resource $ann, float $sarprop_weight_decay_shift): bool
```

Встановлює зміщення загасання sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_weight_decay_shift`

Зміщення загасання sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_sarprop\_weight\_decay\_shift()](function.fann-get-sarprop-weight-decay-shift.md) \- Повертає зсув зменшення ваги sarprop
