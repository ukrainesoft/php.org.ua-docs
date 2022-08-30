Встановлює функцію активації для вказаного нейрона та шару

-   [« fannsetactivationfunctionoutput](function.fann-set-activation-function-output.html)
    
-   [fannsetactivationsteepnesshidden »](function.fann-set-activation-steepness-hidden.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Встановлює функцію активації для вказаного нейрона та шару
    

# fannsetactivationfunction

(PECL fann> = 1.0.0)

fannsetactivationfunction — Встановлює функцію активації для вказаного нейрона та шару

### Опис

```methodsynopsis
fann_set_activation_function(    resource $ann,    int $activation_function,    int $layer,    int $neuron): bool
```

Встановіть функцію активації для нейрона номер `neuron` у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

Неможливо встановити функції активації для нейронів у вхідному шарі.

При виборі функції активації важливо враховувати, що функції активації мають різний діапазон . \*\*`FANN_SIGMOID`\*\*наприклад, в діапазоні від 0 до 1, у той час як **`FANN_SIGMOID_SYMMETRIC`** знаходиться в діапазоні від -1 до 1, а **`FANN_LINEAR`** без обмежень.

Надане значення activationfunction має бути однією з констант [функцій активації](fann.constants.html#constants.fann-activation-funcs)

Значення, що повертається - одна з констант [функцій активації](fann.constants.html#constants.fann-train)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_function`

Константа [функцій активації](fann.constants.html#constants.fann-activation-funcs)

`layer`

Номер шару.

`neuron`

Номер нейрона.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationfunctionlayer()](function.fann-set-activation-function-layer.html) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fannsetactivationfunctionhidden()](function.fann-set-activation-function-hidden.html) - Встановлює функцію активації для всіх прихованих шарів
-   [fannsetactivationfunctionoutput()](function.fann-set-activation-function-output.html) - Встановлює функцію активації для вихідного шару
-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fanngetactivationfunction()](function.fann-get-activation-function.html) - Повертає функцію активації