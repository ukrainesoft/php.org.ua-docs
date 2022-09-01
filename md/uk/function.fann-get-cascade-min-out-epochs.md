---
navigation:
  - function.fann-get-cascade-min-cand-epochs.html: « fanngetcascademincandepochs
  - function.fann-get-cascade-num-candidate-groups.html: fanngetcascadenumcandidategroups »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetcascademinoutepochs
---
# fanngetcascademinoutepochs

(PECL fann> = 1.0.0)

fanngetcascademinoutepochs — Повертає мінімальну кількість періодів

### Опис

```methodsynopsis
fann_get_cascade_min_out_epochs(resource $ann): int
```

Мінімальна кількість періодів визначає кількість періодів, у яких вихідні з'єднання мають бути навчені після додавання нового нейрона-кандидата.

Мінімальна кількість періодів за замовчуванням – 50.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Мінімальна кількість періодів або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannsetcascademinoutepochs()](function.fann-set-cascade-min-out-epochs.html) - Встановлює мінімальні епохи вихідних даних
