Скидає середньоквадратичну помилку з мережі

-   [« fannreseterrstr](function.fann-reset-errstr.html)
    
-   [fannrun »](function.fann-run.html)
    
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

-   [fanngetMSE()](function.fann-get-mse.html) - Зчитує середньоквадратичну помилку мережі
-   [fanngetbitfail()](function.fann-get-bit-fail.html) - Кількість бітів збою
-   [fanngetbitfaillimit()](function.fann-get-bit-fail-limit.html) - Повертає межу збою бітів, використану під час навчання