Повертає функцію активації

-   [« fann\_duplicate\_train\_data](function.fann-duplicate-train-data.html)
    
-   [fann\_get\_activation\_steepness »](function.fann-get-activation-steepness.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
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

Значення, що повертається, є однією з констант [функций активации](fann.constants.html#constants.fann-activation-funcs)

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

-   [fann\_set\_activation\_function\_layer()](function.fann-set-activation-function-layer.html) - Встановлює функцію активації для всіх нейронів у наданому шарі
-   [fann\_set\_activation\_function\_hidden()](function.fann-set-activation-function-hidden.html) - Встановлює функцію активації для всіх прихованих шарів
-   [fann\_set\_activation\_function\_output()](function.fann-set-activation-function-output.html) - Встановлює функцію активації для вихідного шару
-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fann\_set\_activation\_function()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару