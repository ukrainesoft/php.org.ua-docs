---
navigation:
  - function.fann-num-input-train-data.md: « fann\_num\_input\_train\_data
  - function.fann-print-error.md: fann\_print\_error »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_num\_output\_train\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_num\_output\_train\_data

(PECL fann >= 1.0.0)

fann\_num\_output\_train\_data — Повертає кількість вихідних даних у кожному із шаблонів у навчальних даних

### Опис

```methodsynopsis
fann_num_output_train_data(resource $data): int
```

Повертає кількість вихідних даних у кожному із шаблонів у ресурсі (resource) навчальних даних.

### Список параметрів

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Кількість вихідних даних або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_length\_train\_data()](function.fann-length-train-data.md) \- Повертає кількість шаблонів у навчальних даних
-   [fann\_num\_input\_train\_data()](function.fann-num-input-train-data.md) \- Повертає кількість вхідних даних у кожному із шаблонів у навчальних даних
