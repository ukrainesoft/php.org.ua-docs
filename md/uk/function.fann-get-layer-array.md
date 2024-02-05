---
navigation:
  - function.fann-get-errstr.md: « fann\_get\_errstr
  - function.fann-get-learning-momentum.md: fann\_get\_learning\_momentum »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_layer\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_layer\_array

(PECL fann >= 1.0.0)

fann\_get\_layer\_array — Отримує кількість нейронів у кожному шарі мережі

### Опис

```methodsynopsis
fann_get_layer_array(resource $ann): array
```

Отримує кількість нейронів у кожному шарі мережі.

Зміщення не включене, тому шари відповідають функцій fann\_create.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Масив чисел нейтронів у кожному шарі.
