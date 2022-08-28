Встановлює функцію помилки під час тренування.

-   [« fann\_set\_scaling\_params](function.fann-set-scaling-params.html)
    
-   [fann\_set\_train\_stop\_function »](function.fann-set-train-stop-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює функцію помилки під час тренування.
    

# fannsettrainerrorfunction

(PECL fann> = 1.0.0)

fannsettrainerrorfunction — Встановлює функцію помилки під час тренування.

### Опис

```methodsynopsis
fann_set_train_error_function(resource $ann, int $error_function): bool
```

Встановлює функцію помилки під час тренування.

Функції помилок описані далі у константах [функций ошибок](fann.constants.html#constants.fann-errorfunc)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`error_function`

Константа [функций ошибок](fann.constants.html#constants.fann-errorfunc)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_train\_error\_function()](function.fann-get-train-error-function.html) - Повертає функцію обробки помилок, що використовується під час навчання