---
navigation:
  - function.fann-length-train-data.md: « fann\_length\_train\_data
  - function.fann-num-input-train-data.md: fann\_num\_input\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_merge\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_merge\_train\_data

(PECL fann >= 1.0.0)

fann\_merge\_train\_data — Об'єднує навчальні дані

### Опис

```methodsynopsis
fann_merge_train_data(resource $data1, resource $data2): resource
```

Об'єднує дані з data1 і data2 у новий ресурс (resource) навчальних даних.

### Список параметрів

`data1`

Ресурс (resource) навчальних даних нейронної мережі.

`data2`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Новий ресурс (resource) об'єднаних навчальних даних або \*\*`false`\*\*в случае возникновения ошибки.
