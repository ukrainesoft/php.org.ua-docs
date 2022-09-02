---
navigation:
  - function.fann-subset-train-data.md: « fannsubsettraindata
  - function.fann-test.md: fanntest »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanntestdata
---
# fanntestdata

(PECL fann> = 1.0.0)

fanntestdata — Тестування набору навчальних даних та обчислення MSE для нього

### Опис

```methodsynopsis
fann_test_data(resource $ann, resource $data): float
```

Тестування набору навчальних даних та обчислення MSE для нього.

Ця функція оновлює MSE і значення біт невдачі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Оновлена ​​MSE, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanntrainвінdata()](function.fann-train-on-data.md) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanntrainepoch()](function.fann-train-epoch.md) - Навчання протягом однієї епохи
-   [fanngetbitfail()](function.fann-get-bit-fail.md) - Кількість бітів збою
-   [fanngetMSE()](function.fann-get-mse.md) - Зчитує середньоквадратичну помилку мережі
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.md) - встановлює алгоритм навчання
