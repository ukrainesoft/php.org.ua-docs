Встановлює функцію активації для всіх нейронів у наданому шарі

-   [« fannsetactivationfunctionhidden](function.fann-set-activation-function-hidden.html)
    
-   [fannsetactivationfunctionoutput »](function.fann-set-activation-function-output.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює функцію активації для всіх нейронів у наданому шарі
    

# fannsetactivationfunctionlayer

(PECL fann> = 1.0.0)

fannsetactivationfunctionlayer — Встановлює функцію активації для всіх нейронів у наданому шарі

### Опис

```methodsynopsis
fann_set_activation_function_layer(resource $ann, int $activation_function, int $layer): bool
```

Встановіть функцію активації всіх нейронів у шарі номер `layer`, Вважаючи вхідний шар шаром 0.

Неможливо встановити функції активації для нейронів у вхідному шарі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_function`

Константа [функцій активації](fann.constants.html#constants.fann-activation-funcs)

`layer`

Номер шару.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationfunction()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару
-   [fannsetactivationfunctionhidden()](function.fann-set-activation-function-hidden.html) - Встановлює функцію активації для всіх прихованих шарів
-   [fannsetactivationfunctionoutput()](function.fann-set-activation-function-output.html) - Встановлює функцію активації для вихідного шару
-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару