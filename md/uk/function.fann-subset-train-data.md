---
navigation:
  - function.fann-shuffle-train-data.md: « fann\_shuffle\_train\_data
  - function.fann-test-data.md: fann\_test\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_subset\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_subset\_train\_data

(PECL fann >= 1.0.0)

fann\_subset\_train\_data — Отримати копію підмножини з навчальних даних

### Опис

```methodsynopsis
fann_subset_train_data(resource $data, int $pos, int $length): resource
```

Повертає копію підмножини з навчальних даних resource, що починаються з `pos` та довжиною `length` елементів.

`fann_subset_train_data(train_data, 0, fann_length_train_data(train_data))` робить те саме, що і [fann\_duplicate\_train\_data()](function.fann-duplicate-train-data.md)

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

`pos`

Початкова позиція.

`length`

Кількість елементів, що копіюються.

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_duplicate\_train\_data()](function.fann-duplicate-train-data.md) \- Повертає точну копію тренувальних даних
