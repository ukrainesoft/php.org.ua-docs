---
navigation:
  - function.fann-destroy.md: « fann\_destroy
  - function.fann-get-activation-function.md: fann\_get\_activation\_function »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_duplicate\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_duplicate\_train\_data

(PECL fann >= 1.0.0)

fann\_duplicate\_train\_data — Повертає точну копію тренувальних даних

### Опис

```methodsynopsis
fann_duplicate_train_data(resource $data): resource
```

Повертає ресурс (resource) з точною копією тренувальних даних

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або \*\*`false`\*\*в случае возникновения ошибки.
