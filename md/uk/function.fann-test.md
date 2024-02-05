---
navigation:
  - function.fann-test-data.md: « fann\_test\_data
  - function.fann-train-epoch.md: fann\_train\_epoch »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_test
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_test

(PECL fann >= 1.0.0)

fann\_test — Тестування з набором вхідних даних та бажаним результатом

### Опис

```methodsynopsis
fann_test(resource $ann, array $input, array $desired_output): array
```

Тестування з набором вхідних даних та бажаним результатом. Ця операція оновить середньоквадратичну помилку, але не змінить мережу.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input`

Масив вхідних даних. Розмір масиву має точно відповідати [fann\_get\_num\_input()](function.fann-get-num-input.md)

`desired_output`

Масив бажаних результатів. Розмір масиву має точно відповідати [fann\_get\_num\_output()](function.fann-get-num-output.md)

### Значення, що повертаються

Повертає тестові висновки у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки

### Дивіться також

-   [fann\_test\_data()](function.fann-test-data.md) \- Тестування набору навчальних даних та обчислення MSE для нього
-   [fann\_train()](function.fann-train.md) \- Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом
-   [fann\_get\_num\_input()](function.fann-get-num-input.md) \- Отримує кількість вхідних нейронів
-   [fann\_get\_num\_output()](function.fann-get-num-output.md) \- Отримує кількість вихідних нейронів
