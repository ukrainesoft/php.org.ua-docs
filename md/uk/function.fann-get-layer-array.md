---
navigation:
  - function.fann-get-errstr.html: « fanngeterrstr
  - function.fann-get-learning-momentum.html: fanngetlearningmomentum »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetlayerarray
---
# fanngetlayerarray

(PECL fann> = 1.0.0)

fanngetlayerarray — Отримує кількість нейронів у кожному шарі мережі

### Опис

```methodsynopsis
fann_get_layer_array(resource $ann): array
```

Отримує кількість нейронів у кожному шарі мережі.

Зміщення не включене, тому шари відповідають функцій fanncreate.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Масив чисел нейтронів у кожному шарі.
