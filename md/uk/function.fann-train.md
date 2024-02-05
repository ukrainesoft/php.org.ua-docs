---
navigation:
  - function.fann-train-on-file.md: « fann\_train\_on\_file
  - class.fannconnection.md: FANNConnection »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_train
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_train

(PECL fann >= 1.0.0)

fann\_train — Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом

### Опис

```methodsynopsis
fann_train(resource $ann, array $input, array $desired_output): bool
```

Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом. Це навчання завжди інкрементальне, тому що представлена ​​лише одна модель.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input`

Масив вхідних даних. Розмір масиву має точно відповідати [fann\_get\_num\_input()](function.fann-get-num-input.md)

`desired_output`

Масив бажаних результатів. Розмір масиву має точно відповідати [fann\_get\_num\_output()](function.fann-get-num-output.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_train\_epoch()](function.fann-train-epoch.md) \- Навчання протягом однієї епохи
-   [fann\_get\_num\_input()](function.fann-get-num-input.md) \- Отримує кількість вхідних нейронів
-   [fann\_get\_num\_output()](function.fann-get-num-output.md) \- Отримує кількість вихідних нейронів
