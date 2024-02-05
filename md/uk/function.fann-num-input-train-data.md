---
navigation:
  - function.fann-merge-train-data.md: « fann\_merge\_train\_data
  - function.fann-num-output-train-data.md: fann\_num\_output\_train\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_num\_input\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_num\_input\_train\_data

(PECL fann >= 1.0.0)

fann\_num\_input\_train\_data — Повертає кількість вхідних даних у кожному шаблоні до навчальних даних.

### Опис

```methodsynopsis
fann_num_input_train_data(resource $data): int
```

Повертає кількість вхідних даних у кожному із шаблонів у ресурсі (resource) навчальних даних.

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Кількість вхідних даних або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_length\_train\_data()](function.fann-length-train-data.md) \- Повертає кількість шаблонів у навчальних даних
-   [fann\_num\_output\_train\_data()](function.fann-num-output-train-data.md) \- Повертає кількість вихідних даних у кожному із шаблонів у навчальних даних
