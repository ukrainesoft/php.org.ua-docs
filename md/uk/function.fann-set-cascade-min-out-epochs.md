---
navigation:
  - function.fann-set-cascade-min-cand-epochs.html: « fannsetcascademincandepochs
  - function.fann-set-cascade-num-candidate-groups.html: fannsetcascadenumcandidategroups »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetcascademinoutepochs
---
# fannsetcascademinoutepochs

(PECL fann> = 1.0.0)

fannsetcascademinoutepochs - Встановлює мінімальні епохи вихідних даних

### Опис

```methodsynopsis
fann_set_cascade_min_out_epochs(resource $ann, int $cascade_min_out_epochs): bool
```

Встановлює мінімальні доби вихідних даних.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`cascade_min_out_epochs`

Мінімальні епохи вихідних даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fanngetcascademinoutepochs()](function.fann-get-cascade-min-out-epochs.html) - Повертає мінімальну кількість періодів
