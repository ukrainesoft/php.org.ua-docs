---
navigation:
  - function.fann-set-rprop-increase-factor.md: « fann\_set\_rprop\_increase\_factor
  - function.fann-set-sarprop-step-error-threshold-factor.md: fann\_set\_sarprop\_step\_error\_threshold\_factor »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_sarprop\_step\_error\_shift
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_sarprop\_step\_error\_shift

(PECL fann >= 1.0.0)

fann\_set\_sarprop\_step\_error\_shift - Встановлює зрушення помилки кроку sarprop

### Опис

```methodsynopsis
fann_set_sarprop_step_error_shift(resource $ann, float $sarprop_step_error_shift): bool
```

Встановлює зрушення помилки кроку sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_step_error_shift`

Зрушення помилки кроку sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_get\_sarprop\_step\_error\_shift()](function.fann-get-sarprop-step-error-shift.md) \- Повертає зрушення помилки кроку sarprop
