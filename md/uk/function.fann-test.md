---
navigation:
  - function.fann-test-data.html: « fanntestdata
  - function.fann-train-epoch.html: fanntrainepoch »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanntest
---
# fanntest

(PECL fann> = 1.0.0)

fanntest — Тестування з набором вхідних даних та бажаним результатом

### Опис

```methodsynopsis
fann_test(resource $ann, array $input, array $desired_output): array
```

Тестування з набором вхідних даних та бажаним результатом. Ця операція оновить середньоквадратичну помилку, але не змінить мережу.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`input`

Масив вхідних даних. Розмір масиву має точно відповідати [fanngetnuminput()](function.fann-get-num-input.html)

`desired_output`

Масив бажаних результатів. Розмір масиву має точно відповідати [fanngetnumoutput()](function.fann-get-num-output.html)

### Значення, що повертаються

Повертає тестові висновки у разі успішного виконання або **`false`** у разі виникнення помилки

### Дивіться також

-   [fanntestdata()](function.fann-test-data.html) - Тестування набору навчальних даних та обчислення MSE для нього
-   [fanntrain()](function.fann-train.html) - Провести одну ітерацію навчання з набором вхідних даних та бажаним результатом
-   [fanngetnuminput()](function.fann-get-num-input.html) - Отримує кількість вхідних нейронів
-   [fanngetnumoutput()](function.fann-get-num-output.html) - Отримує кількість вихідних нейронів
