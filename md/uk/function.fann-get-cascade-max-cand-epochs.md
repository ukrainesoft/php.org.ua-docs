---
navigation:
  - function.fann-get-cascade-candidate-stagnation-epochs.md: « fanngetcascadecandidatestagnationepochs
  - function.fann-get-cascade-max-out-epochs.md: fanngetcascademaxoutepochs »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetcascademaxcandepochs
---
# fanngetcascademaxcandepochs

(PECL fann> = 1.0.0)

fanngetcascademaxcandepochs - Отримує найбільший період кандидата

### Опис

```methodsynopsis
fann_get_cascade_max_cand_epochs(resource $ann): int
```

Максимальний період кандидата визначає максимальну кількість періодів, у яких вхідні з'єднання з кандидатами можуть бути навчені перед додаванням нового нейрона-кандидата.

Максимальний період кандидата за умовчанням – 150.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Максимальний період кандидата чи **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascademaxcandepochs()](function.fann-set-cascade-max-cand-epochs.md) - встановлює найбільший період кандидата
