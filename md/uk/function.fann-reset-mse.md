Скидає середньоквадратичну помилку з мережі

-   [« fann\_reset\_errstr](function.fann-reset-errstr.html)
    
-   [fann\_run »](function.fann-run.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Скидає середньоквадратичну помилку з мережі
    

# fannresetMSE

(PECL fann> = 1.0.0)

fannresetMSE — Скидає середньоквадратичну помилку з мережі

### Опис

```methodsynopsis
fann_reset_MSE(string $ann): bool
```

Скидає середньоквадратичну помилку з мережі.

Функція також скидає кількість бітів, що вийшли з ладу.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_MSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fann\_get\_bit\_fail()](function.fann-get-bit-fail.html) - Кількість бітів збою
-   [fann\_get\_bit\_fail\_limit()](function.fann-get-bit-fail-limit.html) - Повертає межу збою бітів, використану під час навчання