---
navigation:
  - function.fann-destroy-train.html: « fanndestroytrain
  - function.fann-duplicate-train-data.html: fannduplicatetraindata »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanndestroy
---
# fanndestroy

(PECL fann> = 1.0.0)

fanndestroy — Знищує всю мережу та правильно звільняє всю пов'язану пам'ять

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
