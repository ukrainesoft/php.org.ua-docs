Встановлює крутість активації для всіх нейронів у вказаному номері шару

-   [« fann\_set\_activation\_steepness\_hidden](function.fann-set-activation-steepness-hidden.html)
    
-   [fann\_set\_activation\_steepness\_output »](function.fann-set-activation-steepness-output.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює крутість активації для всіх нейронів у вказаному номері шару
    

# fannsetactivationsteepnesslayer

(PECL fann> = 1.0.0)

fannsetactivationsteepnesslayer — Встановлює крутизну активації для всіх нейронів у вказаному номері шару

### Опис

```methodsynopsis
fann_set_activation_steepness_layer(resource $ann, float $activation_steepness, int $layer): bool
```

Встановіть крутість активації для всіх нейронів у шарі номер `layer`, Вважаючи вхідний шар як шар 0.

Неможливо встановити крутість активації нейронів у вхідному шарі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_steepness`

Крутизна активації.

`layer`

Номер шару.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_set\_activation\_steepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fann\_set\_activation\_steepness\_hidden()](function.fann-set-activation-steepness-hidden.html) - Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fann\_set\_activation\_steepness\_output()](function.fann-set-activation-steepness-output.html) - Встановлює крутість активації у вихідному шарі
-   [fann\_get\_activation\_steepness()](function.fann-get-activation-steepness.html) - Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fann\_set\_activation\_function()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару