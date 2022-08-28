Встановлює функцію активації для вихідного шару

-   [« fann\_set\_activation\_function\_layer](function.fann-set-activation-function-layer.html)
    
-   [fann\_set\_activation\_function »](function.fann-set-activation-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює функцію активації для вихідного шару
    

# fannsetactivationfunctionoutput

(PECL fann> = 1.0.0)

fannsetactivationfunctionoutput — Встановлює функцію активації для вихідного шару

### Опис

```methodsynopsis
fann_set_activation_function_output(resource $ann, int $activation_function): bool
```

Встановлює функцію активації вихідного шару.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_function`

Константа [функций активации](fann.constants.html#constants.fann-activation-funcs)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_activation\_function()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару
-   [fann\_set\_activation\_function\_layer()](function.fann-set-activation-function-layer.html) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fann\_set\_activation\_function\_hidden()](function.fann-set-activation-function-hidden.html) - Встановлює функцію активації для всіх прихованих шарів
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару