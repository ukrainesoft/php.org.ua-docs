---
navigation:
  - function.fann-get-sarprop-step-error-shift.md: « fann\_get\_sarprop\_step\_error\_shift
  - function.fann-get-sarprop-temperature.md: fann\_get\_sarprop\_temperature »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_sarprop\_step\_error\_threshold\_factor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_sarprop\_step\_error\_threshold\_factor

(PECL fann >= 1.0.0)

fann\_get\_sarprop\_step\_error\_threshold\_factor - Повертає пороговий коефіцієнт помилки кроку sarprop

### Опис

```methodsynopsis
fann_get_sarprop_step_error_threshold_factor(resource $ann): float
```

Повертає пороговий коефіцієнт помилки кроку sarprop.

Коефіцієнт за замовчуванням становить 0,1.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Пороговий коефіцієнт помилки кроку або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_sarprop\_step\_error\_threshold\_factor()](function.fann-set-sarprop-step-error-threshold-factor.md) \- Встановлює пороговий коефіцієнт помилки кроку sarprop
