---
navigation:
  - function.fann-get-rprop-increase-factor.md: « fann\_get\_rprop\_increase\_factor
  - function.fann-get-sarprop-step-error-threshold-factor.md: fann\_get\_sarprop\_step\_error\_threshold\_factor »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_sarprop\_step\_error\_shift
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_sarprop\_step\_error\_shift

(PECL fann >= 1.0.0)

fann\_get\_sarprop\_step\_error\_shift — Повертає помилку зрушення кроку sarprop

### Опис

```methodsynopsis
fann_get_sarprop_step_error_shift(resource $ann): float
```

Повертає зрушення помилки кроку sarprop.

Зсув помилки кроку за умовчанням становить 1385.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Сдвиг ошибки шага sarprop или\*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_sarprop\_step\_error\_shift()](function.fann-set-sarprop-step-error-shift.md) \- Встановлює зрушення помилки кроку sarprop
