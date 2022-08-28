Кількість бітів збою

-   [« fann\_get\_bit\_fail\_limit](function.fann-get-bit-fail-limit.html)
    
-   [fann\_get\_cascade\_activation\_functions\_count »](function.fann-get-cascade-activation-functions-count.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Кількість бітів збою
    

# fanngetbitfail

(PECL fann> = 1.0.0)

fanngetbitfail - Кількість бітів збою

### Опис

```methodsynopsis
fann_get_bit_fail(resource $ann): int
```

Кількість бітів збою; означає число вихідних нейронів, які відрізняються більше, ніж межа збою бітів (див. [fann\_get\_bit\_fail\_limit()](function.fann-get-bit-fail-limit.html) [fann\_set\_bit\_fail\_limit()](function.fann-set-bit-fail-limit.html)). Біти враховуються у всіх навчальних даних, тому це число може бути більше за кількість навчальних даних.

Це значення скидається [fann\_reset\_MSE()](function.fann-reset-mse.html) і оновлюється всіма тими самими функціями, які також оновлюють значення MSE (наприклад, [fann\_test\_data()](function.fann-test-data.html) [fann\_train\_epoch()](function.fann-train-epoch.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Кількість бітів збою або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_get\_MSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fann\_reset\_MSE()](function.fann-reset-mse.html) - скидає середньоквадратичну помилку з мережі
-   [fann\_test\_data()](function.fann-test-data.html) - Тестування набору навчальних даних та обчислення MSE для нього
-   [fann\_train\_epoch()](function.fann-train-epoch.html) - Навчання протягом однієї епохи
-   [fann\_get\_bit\_fail\_limit()](function.fann-get-bit-fail-limit.html) - Повертає межу збою бітів, використану під час навчання
-   [fann\_set\_bit\_fail\_limit()](function.fann-set-bit-fail-limit.html) - Встановлює межу помилок, що використовується під час навчання