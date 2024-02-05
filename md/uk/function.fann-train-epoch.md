---
navigation:
  - function.fann-test.md: « fann\_test
  - function.fann-train-on-data.md: fann\_train\_on\_data »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_train\_epoch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_train\_epoch

(PECL fann >= 1.0.0)

fann\_train\_epoch - Навчання протягом однієї епохи

### Опис

```methodsynopsis
fann_train_epoch(resource $ann, resource $data): float
```

Навчання протягом однієї доби. Одна епоха визначає, що всі навчальні дані будуть використані рівно один раз.

Ця функція повертає повідомлення про помилку MSE, що розраховується до або під час фактичного навчання. Не актуальне значення MSE, пораховане після навчання протягом епохи, але, оскільки його розрахунку довелося б перебрати навчальний набір вкотре, то зручніше використовувати це значення.

Алгоритм навчання використовуваний цією функцією вибирається за допомогою [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`data`

Ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

MSE или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.md) \- Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_test\_data()](function.fann-test-data.md) \- Тестування набору навчальних даних та обчислення MSE для нього
-   [fann\_get\_MSE()](function.fann-get-mse.md) \- Зчитує середньоквадратичну помилку мережі
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
