---
navigation:
  - function.fann-set-sarprop-step-error-shift.md: « fann\_set\_sarprop\_step\_error\_shift
  - function.fann-set-sarprop-temperature.md: fann\_set\_sarprop\_temperature »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_sarprop\_step\_error\_threshold\_factor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_sarprop\_step\_error\_threshold\_factor

(PECL fann >= 1.0.0)

fann\_set\_sarprop\_step\_error\_threshold\_factor — Встановлює пороговий коефіцієнт помилки кроку sarprop

### Опис

```methodsynopsis
fann_set_sarprop_step_error_threshold_factor(resource $ann, float $sarprop_step_error_threshold_factor): bool
```

Встановлює пороговий коефіцієнт помилки кроку sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_step_error_threshold_factor`

Пороговий коефіцієнт помилки кроку sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_sarprop\_step\_error\_threshold\_factor()](function.fann-get-sarprop-step-error-threshold-factor.md) \- Повертає пороговий коефіцієнт помилки кроку sarprop
