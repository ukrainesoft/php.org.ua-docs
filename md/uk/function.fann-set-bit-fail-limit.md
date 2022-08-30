Встановлює межу помилок, що використовується під час навчання

-   [« fannsetactivationsteepness](function.fann-set-activation-steepness.html)
    
-   [fannsetcallback »](function.fann-set-callback.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Встановлює межу помилок, що використовується під час навчання
    

# fannsetbitfaillimit

(PECL fann> = 1.0.0)

fannsetbitfaillimit — Встановлює межу помилок, що використовується під час навчання

### Опис

```methodsynopsis
fann_set_bit_fail_limit(resource $ann, float $bit_fail_limit): bool
```

Встановлює межу помилок, яка використовується під час навчання.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`bit_fail_limit`

Межа помилок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetbitfaillimit()](function.fann-get-bit-fail-limit.html) - Повертає межу збою бітів, використану під час навчання