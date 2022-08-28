Встановлює коефіцієнт збільшення під час навчання Rprop

-   [« fann\_set\_rprop\_delta\_zero](function.fann-set-rprop-delta-zero.html)
    
-   [fann\_set\_sarprop\_step\_error\_shift »](function.fann-set-sarprop-step-error-shift.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює коефіцієнт збільшення під час навчання Rprop
    

# fannsetrpropincreasefactor

(PECL fann> = 1.0.0)

fannsetrpropincreasefactor — Встановлює коефіцієнт збільшення, який використовується під час навчання Rprop

### Опис

```methodsynopsis
fann_set_rprop_increase_factor(resource $ann, float $rprop_increase_factor): bool
```

Встановлює коефіцієнт збільшення під час навчання Rprop

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_increase_factor`

Коефіцієнт збільшення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_rprop\_increase\_factor()](function.fann-get-rprop-increase-factor.html) - Повертає коефіцієнт збільшення, який використовується під час навчання RPROP