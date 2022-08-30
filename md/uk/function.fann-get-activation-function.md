Повертає функцію активації

-   [« fannduplicatetraindata](function.fann-duplicate-train-data.html)
    
-   [fanngetactivationsteepness »](function.fann-get-activation-steepness.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Повертає функцію активації
    

# fanngetactivationfunction

(PECL fann> = 1.0.0)

fanngetactivationfunction — Повертає функцію активації

### Опис

```methodsynopsis
fann_get_activation_function(resource $ann, int $layer, int $neuron): int
```

Отримує функцію активації номера нейрона `neuron` у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

Неможливо отримати функції активації для нейронів у вхідному шарі.

Значення, що повертається, є однією з констант [функцій активації](fann.constants.html#constants.fann-activation-funcs)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`layer`

Номер шару.

`neuron`

Номер нейрона.

### Значення, що повертаються

Константа [функций обучения](fann.constants.html#constants.fann-train) або -1, якщо нейрон не визначений у нейронній мережі або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetactivationfunctionlayer()](function.fann-set-activation-function-layer.html) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fannsetactivationfunctionhidden()](function.fann-set-activation-function-hidden.html) - Встановлює функцію активації для всіх прихованих шарів
-   [fannsetactivationfunctionoutput()](function.fann-set-activation-function-output.html) - Встановлює функцію активації для вихідного шару
-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fannsetactivationfunction()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару