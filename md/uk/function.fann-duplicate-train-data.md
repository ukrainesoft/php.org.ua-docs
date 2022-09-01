---
navigation:
  - function.fann-destroy.html: « fanndestroy
  - function.fann-get-activation-function.html: fanngetactivationfunction »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannduplicatetraindata
---
# fannduplicatetraindata

(PECL fann> = 1.0.0)

fannduplicatetraindata — Повертає точну копію тренувальних даних

### Опис

```methodsynopsis
fann_duplicate_train_data(resource $data): resource
```

Повертає ресурс (resource) з точною копією тренувальних даних

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або **`false`** у разі виникнення помилки.
