---
navigation:
  - function.fann-train-on-file.html: « fanntrainвінfile
  - class.fannconnection.md: FANNConnection »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanntrain
---
# fanntrain

(PECL fann> = 1.0.0)

fanntrain — Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом

### Опис

```methodsynopsis
fann_train(resource $ann, array $input, array $desired_output): bool
```

Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом. Це навчання завжди інкрементальне, тому що представлена ​​лише одна модель.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input`

Масив вхідних даних. Розмір масиву має точно відповідати [fanngetnuminput()](function.fann-get-num-input.html)

`desired_output`

Масив бажаних результатів. Розмір масиву має точно відповідати [fanngetnumoutput()](function.fann-get-num-output.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanntrainвінdata()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanntrainepoch()](function.fann-train-epoch.html) - Навчання протягом однієї епохи
-   [fanngetnuminput()](function.fann-get-num-input.html) - Отримує кількість вхідних нейронів
-   [fanngetnumoutput()](function.fann-get-num-output.html) - Отримує кількість вихідних нейронів
