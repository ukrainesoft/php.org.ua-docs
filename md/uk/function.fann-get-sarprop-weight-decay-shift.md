---
navigation:
  - function.fann-get-sarprop-temperature.md: « fann\_get\_sarprop\_temperature
  - function.fann-get-total-connections.md: fann\_get\_total\_connections »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_sarprop\_weight\_decay\_shift
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_sarprop\_weight\_decay\_shift

(PECL fann >= 1.0.0)

fann\_get\_sarprop\_weight\_decay\_shift — Повертає зменшення ваги sarprop

### Опис

```methodsynopsis
fann_get_sarprop_weight_decay_shift(resource $ann): float
```

Повертає зсув зменшення ваги sarprop.

Максимальна дельта за промовчанням становить -6.644.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Сдвиг уменьшения веса sarprop или\*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fann\_set\_sarprop\_weight\_decay\_shift()](function.fann-set-sarprop-weight-decay-shift.md) \- Встановлює зміщення згасання sarprop
