---
navigation:
  - function.fann-test.html: « fanntest
  - function.fann-train-on-data.html: fanntrainвінdata »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanntrainepoch
---
# fanntrainepoch

(PECL fann> = 1.0.0)

fanntrainepoch - Навчання протягом однієї епохи

### Опис

```methodsynopsis
fann_train_epoch(resource $ann, resource $data): float
```

Навчання протягом однієї доби. Одна епоха визначає, що всі навчальні дані будуть використані рівно один раз.

Ця функція повертає повідомлення про помилку MSE, що розраховується до або під час фактичного навчання. Не актуальне значення MSE, пораховане після навчання протягом епохи, але, оскільки його розрахунку довелося б перебрати навчальний набір вкотре, то зручніше використовувати це значення.

Алгоритм навчання використовуваний цією функцією вибирається за допомогою [fannsettrainingalgorithm()](function.fann-set-training-algorithm.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

MSE або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanntrainвінdata()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanntestdata()](function.fann-test-data.html) - Тестування набору навчальних даних та обчислення MSE для нього
-   [fanngetMSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.html) - встановлює алгоритм навчання
