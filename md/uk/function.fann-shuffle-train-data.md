---
navigation:
  - function.fann-set-weight.md: « fann\_set\_weight
  - function.fann-subset-train-data.md: fann\_subset\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_shuffle\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_shuffle\_train\_data

(PECL fann >= 1.0.0)

fann\_shuffle\_train\_data — Перемішує навчальні дані у випадковому порядку

### Опис

```methodsynopsis
fann_shuffle_train_data(resource $train_data): bool
```

Перемішує навчальні дані у випадковому порядку. Рекомендується використовувати при інкрементальному навчанні, але не впливає на пакетне навчання.

### Список параметрів

`train_data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.
