---
navigation:
  - function.fann-subset-train-data.md: « fann\_subset\_train\_data
  - function.fann-test.md: fann\_test »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_test\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_test\_data

(PECL fann >= 1.0.0)

fann\_test\_data — Тестування набору навчальних даних та обчислення MSE для нього

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

Оновлена ​​MSE, або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_train\_epoch()](function.fann-train-epoch.md) \- Навчання протягом однієї епохи
-   [fann\_get\_bit\_fail()](function.fann-get-bit-fail.md) \- Кількість бітів збою
-   [fann\_get\_MSE()](function.fann-get-mse.md) \- Зчитує середньоквадратичну помилку мережі
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
