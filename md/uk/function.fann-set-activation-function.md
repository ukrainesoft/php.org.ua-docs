Встановлює функцію активації для вказаного нейрона та шару

-   [« fann\_set\_activation\_function\_output](function.fann-set-activation-function-output.html)
    
-   [fann\_set\_activation\_steepness\_hidden »](function.fann-set-activation-steepness-hidden.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
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

При виборі функції активації важливо враховувати, що функції активації мають різний діапазон . **`FANN_SIGMOID`**наприклад, в діапазоні від 0 до 1, у той час як **`FANN_SIGMOID_SYMMETRIC`** знаходиться в діапазоні від -1 до 1, а **`FANN_LINEAR`** без обмежень.

Надане значення activationfunction має бути однією з констант [функций активации](fann.constants.html#constants.fann-activation-funcs)

Значення, що повертається - одна з констант [функций активации](fann.constants.html#constants.fann-train)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_function`

Константа [функций активации](fann.constants.html#constants.fann-activation-funcs)

`layer`

Номер шару.

`neuron`

Номер нейрона.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_activation\_function\_layer()](function.fann-set-activation-function-layer.html) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fann\_set\_activation\_function\_hidden()](function.fann-set-activation-function-hidden.html) - Встановлює функцію активації для всіх прихованих шарів
-   [fann\_set\_activation\_function\_output()](function.fann-set-activation-function-output.html) - Встановлює функцію активації для вихідного шару
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fann\_get\_activation\_function()](function.fann-get-activation-function.html) - Повертає функцію активації