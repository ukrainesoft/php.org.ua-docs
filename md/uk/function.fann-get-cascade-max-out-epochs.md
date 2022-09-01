---
navigation:
  - function.fann-get-cascade-max-cand-epochs.html: « fanngetcascademaxcandepochs
  - function.fann-get-cascade-min-cand-epochs.html: fanngetcascademincandepochs »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
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

-   [fannsetcascademaxoutepochs()](function.fann-set-cascade-max-out-epochs.html) - Встановлює максимальну кількість епох
