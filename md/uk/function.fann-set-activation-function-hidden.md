Встановлює функцію активації для всіх прихованих шарів

-   [« fannscaletrain](function.fann-scale-train.html)
    
-   [fannsetactivationfunctionlayer »](function.fann-set-activation-function-layer.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
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

Константа [функцій активації](fann.constants.html#constants.fann-activation-funcs)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationfunction()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару
-   [fannsetactivationfunctionlayer()](function.fann-set-activation-function-layer.html) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fannsetactivationfunctionoutput()](function.fann-set-activation-function-output.html) - Встановлює функцію активації для вихідного шару
-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару