---
navigation:
  - function.fann-get-bit-fail-limit.md: « fann\_get\_bit\_fail\_limit
  - function.fann-get-cascade-activation-functions-count.md: fann\_get\_cascade\_activation\_functions\_count »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_bit\_fail
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_bit\_fail

(PECL fann >= 1.0.0)

fann\_get\_bit\_fail - Кількість бітів збою

### Опис

```methodsynopsis
fann_get_bit_fail(resource $ann): int
```

Кількість бітів збою; означає кількість вихідних нейронів, які відрізняються більше, ніж межа збою бітів (див. [fann\_get\_bit\_fail\_limit()](function.fann-get-bit-fail-limit.md) [fann\_set\_bit\_fail\_limit()](function.fann-set-bit-fail-limit.md)). Біти враховуються у всіх навчальних даних, тому це число може бути більше за кількість навчальних даних.

Це значення скидається [fann\_reset\_MSE()](function.fann-reset-mse.md) і оновлюється всіма тими самими функціями, які також оновлюють значення MSE (наприклад, [fann\_test\_data()](function.fann-test-data.md) [fann\_train\_epoch()](function.fann-train-epoch.md)) .

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість бітів збою або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_get\_MSE()](function.fann-get-mse.md) \- Зчитує середньоквадратичну помилку мережі
-   [fann\_reset\_MSE()](function.fann-reset-mse.md) \- скидає середньоквадратичну помилку з мережі
-   [fann\_test\_data()](function.fann-test-data.md) \- Тестування набору навчальних даних та обчислення MSE для нього
-   [fann\_train\_epoch()](function.fann-train-epoch.md) \- Навчання протягом однієї епохи
-   [fann\_get\_bit\_fail\_limit()](function.fann-get-bit-fail-limit.md) \- Повертає межу збою бітів, використану під час навчання
-   [fann\_set\_bit\_fail\_limit()](function.fann-set-bit-fail-limit.md) \- Встановлює межу помилок, що використовується під час навчання
