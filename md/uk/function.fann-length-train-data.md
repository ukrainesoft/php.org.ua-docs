---
navigation:
  - function.fann-init-weights.md: « fann\_init\_weights
  - function.fann-merge-train-data.md: fann\_merge\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_length\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_length\_train\_data

(PECL fann >= 1.0.0)

fann\_length\_train\_data — Повертає кількість шаблонів до навчальних даних

### Опис

```methodsynopsis
fann_length_train_data(resource $data): int
```

Повертає кількість шаблонів у ресурсі (resource) навчальних даних.

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Кількість елементів у ресурсі (resource) навчальних даних або \*\*`false`\*\*в случае возникновения ошибки.
