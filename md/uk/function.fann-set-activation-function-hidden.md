Встановлює функцію активації для всіх прихованих шарів

-   [« fann\_scale\_train](function.fann-scale-train.html)
    
-   [fann\_set\_activation\_function\_layer »](function.fann-set-activation-function-layer.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює функцію активації для всіх прихованих шарів
    

# fannsetactivationfunctionhidden

(PECL fann> = 1.0.0)

fannsetactivationfunctionhidden — Встановлює функцію активації для всіх прихованих шарів

### Опис

```methodsynopsis
fann_set_activation_function_hidden(resource $ann, int $activation_function): bool
```

Встановлює функцію активації всіх прихованих шарів.

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
-   [fann\_set\_activation\_function\_output()](function.fann-set-activation-function-output.html) - Встановлює функцію активації для вихідного шару
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару