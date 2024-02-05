---
navigation:
  - function.fann-get-sarprop-step-error-threshold-factor.md: « fann\_get\_sarprop\_step\_error\_threshold\_factor
  - function.fann-get-sarprop-weight-decay-shift.md: fann\_get\_sarprop\_weight\_decay\_shift »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_sarprop\_temperature
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_sarprop\_temperature

(PECL fann >= 1.0.0)

fann\_get\_sarprop\_temperature - Повертає температуру sarprop

### Опис

```methodsynopsis
fann_get_sarprop_temperature(resource $ann): float
```

Повертає температуру сарprop.

Температура за промовчанням становить 0.015.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Температура sarprop или\*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_sarprop\_temperature()](function.fann-set-sarprop-temperature.md) \- Встановлює температуру sarprop
