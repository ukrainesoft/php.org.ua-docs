---
navigation:
  - function.fann-get-bit-fail-limit.html: « fanngetbitfaillimit
  - function.fann-get-cascade-activation-functions-count.html: fanngetcascadeactivationfunctionscount »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetbitfail
---
# fanngetbitfail

(PECL fann> = 1.0.0)

fanngetbitfail - Кількість бітів збою

### Опис

```methodsynopsis
fann_get_bit_fail(resource $ann): int
```

Кількість бітів збою; означає число вихідних нейронів, які відрізняються більше, ніж межа збою бітів (див. [fanngetbitfaillimit()](function.fann-get-bit-fail-limit.html) [fannsetbitfaillimit()](function.fann-set-bit-fail-limit.html)). Біти враховуються у всіх навчальних даних, тому це число може бути більше за кількість навчальних даних.

Це значення скидається [fannresetMSE()](function.fann-reset-mse.html) і оновлюється всіма тими самими функціями, які також оновлюють значення MSE (наприклад, [fanntestdata()](function.fann-test-data.html) [fanntrainepoch()](function.fann-train-epoch.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість бітів збою або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fanngetMSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fannresetMSE()](function.fann-reset-mse.html) - скидає середньоквадратичну помилку з мережі
-   [fanntestdata()](function.fann-test-data.html) - Тестування набору навчальних даних та обчислення MSE для нього
-   [fanntrainepoch()](function.fann-train-epoch.html) - Навчання протягом однієї епохи
-   [fanngetbitfaillimit()](function.fann-get-bit-fail-limit.html) - Повертає межу збою бітів, використану під час навчання
-   [fannsetbitfaillimit()](function.fann-set-bit-fail-limit.html) - Встановлює межу помилок, що використовується під час навчання
