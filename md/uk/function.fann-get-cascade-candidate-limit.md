---
navigation:
  - function.fann-get-cascade-candidate-change-fraction.html: « fanngetcascadecandidatechangefraction
  - function.fann-get-cascade-candidate-stagnation-epochs.html: fanngetcascadecandidatestagnationepochs »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetcascadecandidatelimit
---
# fanngetcascadecandidatelimit

(PECL fann> = 1.0.0)

fanngetcascadecandidatelimit — Повертає межу кандидата

### Опис

```methodsynopsis
fann_get_cascade_candidate_limit(resource $ann): float
```

Межа кандидата - це межа того, скільки нейронів кандидата може бути навчено. Обмеження – це обмеження на співвідношення між MSE та балом кандидата.

Встановлює це більш низьке значення, щоб уникнути переоснащення, і більш високе, якщо переоснащення перестав бути проблемою.

Гранична кількість кандидатів за умовчанням становить 1000.0.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Межа кандидата або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascadecandidatelimit()](function.fann-set-cascade-candidate-limit.html) - встановлює ліміт кандидатів
