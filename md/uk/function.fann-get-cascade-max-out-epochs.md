---
navigation:
  - function.fann-get-cascade-max-cand-epochs.md: « fanngetcascademaxcandepochs
  - function.fann-get-cascade-min-cand-epochs.md: fanngetcascademincandepochs »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetcascademaxoutepochs
---
# fanngetcascademaxoutepochs

(PECL fann> = 1.0.0)

fanngetcascademaxoutepochs — Повертає максимальну кількість періодів

### Опис

```methodsynopsis
fann_get_cascade_max_out_epochs(resource $ann): int
```

Максимальна кількість періодів визначає кількість періодів, у яких вихідні з'єднання можуть бути навчені після додавання нового нейрона-кандидата.

Максимальна кількість періодів дорівнює 150.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Максимальна кількість періодів або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetcascademaxoutepochs()](function.fann-set-cascade-max-out-epochs.md) - Встановлює максимальну кількість епох
