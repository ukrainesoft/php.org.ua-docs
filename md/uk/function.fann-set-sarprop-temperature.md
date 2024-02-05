---
navigation:
  - function.fann-set-sarprop-step-error-threshold-factor.md: « fann\_set\_sarprop\_step\_error\_threshold\_factor
  - function.fann-set-sarprop-weight-decay-shift.md: fann\_set\_sarprop\_weight\_decay\_shift »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_sarprop\_temperature
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_sarprop\_temperature

(PECL fann >= 1.0.0)

fann\_set\_sarprop\_temperature - Встановлює температуру sarprop

### Опис

```methodsynopsis
fann_set_sarprop_temperature(resource $ann, float $sarprop_temperature): bool
```

Встановлює температуру sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_temperature`

Температура sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_sarprop\_temperature()](function.fann-get-sarprop-temperature.md) \- Повертає температуру sarprop
