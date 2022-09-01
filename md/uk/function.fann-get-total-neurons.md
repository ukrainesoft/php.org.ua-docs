---
navigation:
  - function.fann-get-total-connections.html: « fanngettotalconnections
  - function.fann-get-train-error-function.html: fanngettrainerrorfunction »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngettotalneurons
---
# fanngettotalneurons

(PECL fann> = 1.0.0)

fanngettotalneurons — Отримує загальну кількість нейронів у всій мережі

### Опис

```methodsynopsis
fann_get_total_neurons(resource $ann): int
```

Отримує загальну кількість нейронів у всій мережі. Число також включає нейрони усунення, тому мережа 2-4-2 має 2+4+2 +2 (зміщення) = 10 нейронів.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Загальна кількість нейронів у всій мережі або **`false`** у разі виникнення помилки.
