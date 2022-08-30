Встановлює крутість активації у вихідному шарі

-   [« fannsetactivationsteepnesslayer](function.fann-set-activation-steepness-layer.html)
    
-   [fannsetactivationsteepness »](function.fann-set-activation-steepness.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює крутість активації у вихідному шарі
    

# fannsetactivationsteepnessoutput

(PECL fann> = 1.0.0)

fannsetactivationsteepnessoutput — Встановлює крутість активації у вихідному шарі

### Опис

```methodsynopsis
fann_set_activation_steepness_output(resource $ann, float $activation_steepness): bool
```

Встановлює крутість активації у вихідному шарі.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`activation_steepness`

Крутизна активації.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fannsetactivationsteepness()](function.fann-set-activation-steepness.html) - Встановлює крутість активації для вказаного нейрона та номера шару
-   [fannsetactivationsteepnesslayer()](function.fann-set-activation-steepness-layer.html) - Встановлює крутість активації для всіх нейронів у вказаному номері шару
-   [fannsetactivationsteepnesshidden()](function.fann-set-activation-steepness-hidden.html) - Встановлює крутість крутості активації для всіх нейронів у всіх прихованих шарах
-   [fanngetactivationsteepness()](function.fann-get-activation-steepness.html) - Повертає крутість активації для нейрона, що поставляється, і номери шару
-   [fannsetactivationfunction()](function.fann-set-activation-function.html) - Встановлює функцію активації для зазначеного нейрона та шару