Встановлює функцію активації для вихідного шару

-   [« fannsetactivationfunctionlayer](function.fann-set-activation-function-layer.html)
    
-   [fannsetactivationfunction »](function.fann-set-activation-function.html)
    
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

Константа [функцій активації](fann.constants.html#constants.fann-activation-funcs)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationfunction()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару
-   [fannsetactivationfunctionlayer()](function.fann-set-activation-function-layer.html) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fannsetactivationfunctionhidden()](function.fann-set-activation-function-hidden.html) - Встановлює функцію активації для всіх прихованих шарів
-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару