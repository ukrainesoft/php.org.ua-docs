---
navigation:
  - function.fann-destroy-train.md: « fann\_destroy\_train
  - function.fann-duplicate-train-data.md: fann\_duplicate\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_destroy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_destroy

(PECL fann >= 1.0.0)

fann\_destroy — Знищує всю мережу та правильно звільняє всю пов'язану пам'ять

### Опис

```methodsynopsis
fann_destroy(resource $ann): bool
```

Знищує всю мережу та правильно звільняє всю пов'язану пам'ять.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.
